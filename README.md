# 단열 이상기체 출구온도 계산기

가역 단열 이상기체 과정의 압력비에 따른 온도 계산

- Plan ID: E077
- App: https://nanalab.kr/eng-adiabatic-temperature/
- Repository: https://github.com/NaNaCompany/eng-adiabatic-temperature
- Formula: `T₂ = T₁(p₂/p₁)^((γ−1)/γ)`
- Output: 최종 절대온도 T₂

## Model

T₁,p₁,p₂>0, γ>1. 일정 비열의 이상기체가 가역 단열 과정을 거친다고 가정한다. 비가역 효율·충격파·상변화는 제외하며 게이지압을 쓰지 않는다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `365.704096261343`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
