# CafeSwipe — Geolocalização & Swipe Deck Reativo

Aplicação SPA desenvolvida em **Angular 18+ (Standalone Components + Signals)** e **Tailwind CSS** para descoberta de cafeterias próximas via **Google Maps Places API (New)** com gestos nativos via **Pointer Events API** (zero dependências legadas de touch) e persistência local reativa.

## Decisões de Arquitetura (Frontend Sênior)
- **Estado Reativo Granular com Angular Signals**: Gerenciamento de estado via `signal()`, `computed()` e `effect()` para sincronização automática com `localStorage`.
- **Pointer Events Nativos & Acessibilidade**: Substituição de bibliotecas legadas (`Hammer.js`) por `pointerdown/pointermove/pointerup` + suporte completo via teclado (`ArrowLeft` / `ArrowRight`) e atributos ARIA.
- **Resiliência de API & CORS**: Integração direta com a SDK oficial `google.maps.places.Place.searchNearby` (eliminando problemas de CORS de chamadas REST client-side) e fallback automático para dataset local em ambiente de desenvolvimento.

## Como Executar
```bash
npm install
npm start
```
