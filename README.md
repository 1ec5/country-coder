# country-coder

📍 ➡️ 🇩🇰 Convert longitude-latitude pairs to [ISO 3166-1 codes](https://en.wikipedia.org/wiki/ISO_3166-1) quickly and locally


## What is it?

`country-coder` is a lightweight package that looks up region identifiers for geographic points without calling a server. It can retrieve and convert between several common IDs:

- 🆎 [ISO 3166-1 alpha-2 code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) (`ZA`)
- 🔤 [ISO 3166-1 alpha-3 code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) (`ZAF`)
- 3️⃣ [ISO 3166-1 numeric-3 code](https://en.wikipedia.org/wiki/ISO_3166-1_numeric) (`710`)
- 🌐 [Wikidata QID](https://www.wikidata.org/wiki/Q43649390) (`Q258`)
- 🇺🇳 [Emoji Flag](https://en.wikipedia.org/wiki/Regional_Indicator_Symbol) (🇿🇦)

There are separate endpoints to include non-country ISO 3166-1 features in the query, such as Puerto Rico and the Isle of Man. Some unofficial yet exceptionally-reserved or user-assigned ISO codes are also supported, such as the European Union (`EU`) and Kosovo (`XK`).

#### Advantages

Client-side coding has a number of benefits over server-side solutions:

- ✅ 🚅 *Performance*: get fast, reliable results at scale
- ✅ ✌️ *Ease of Use*: forget async callbacks, network errors, API keys, and rate limits
- ✅ 🕶 *Privacy*: keep your location data on-device
- ✅ 📴 *Offline Workflows*: deploy to connection-challenged environments

#### Caveats

`country-coder` prioritizes package size and lookup speed over precision. Thus, it's **not** suitable for some situations and use cases:

- 🚫 🛂 *Disputed Borders*: only one country is returned per point, the "de facto controlling country"
- 🚫 🚢 *Maritime Borders*: only points on land are supported; borders over water are highly generalized
- 🚫 🖋 *Complex Borders*: land borders are of varying detail and may be imprecise at granular scales
- 🚫 🧩 *Country Subdivisions*: provinces and similar features under ISO 3166-2 cannot be coded
- 🚫 📇 *Naming*: feature names are omitted; get them via another package or the Wikidata API
- 🚫 📐 *Spatial Operations*: a feature's calculated area, bounding box, etc. will likely be inaccurate
- 🚫 🗺 *Mapmaking*: the border data is not intended for rendering


## Installing

`npm install country-coder`

This library is available in both ES5/CommonJS and ES6 module formats.

```js
const CountryCoder = require('country-coder').CountryCoder;   // CommonJS
// or
import { CountryCoder } from 'country-coder';     // ES6
```


## Contributing

This package is kept intentionally minimal. However, if you find a bug or have an interesting idea for an enhancement, feel free to open an [Issue](https://github.com/ideditor/country-coder/issues) and/or [Pull Request](https://github.com/ideditor/country-coder/pulls).
