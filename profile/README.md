<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="brand/logo-white.svg">
    <img src="brand/logo.svg" alt="Idemity" width="260">
  </picture>
</p>

<p align="center">
  <strong>Face recognition as an API.</strong><br>
  Register a face, then verify, identify, and check liveness — over a simple HTTP API, in five languages, on our cloud or your own servers.
</p>

---

## What Idemity does

Idemity turns face recognition into a few API calls, so you can add it to a product without training models or running GPUs yourself.

- **Verify (1:1)** — confirm a face matches a known person.
- **Identify (1:N)** — search a collection and find who a face belongs to.
- **Compare** — score how similar two faces are.
- **Liveness** — tell a real person from a photo or screen replay.
- **Attributes** — age, gender, head pose, emotion, glasses, and mask detection.
- **Collections & batch** — organize enrolled faces per use case; register in bulk, synchronously or as async jobs.

Every request is scoped to an API key, so keys map cleanly to environments and teams.

## SDKs

Official, first-party clients — same API surface, idiomatic in each language:

| Language | Package | Repo |
|---|---|---|
| TypeScript / JavaScript | `idemity` (npm) | [idemity-js](https://github.com/idemity/idemity-js) |
| Python | `idemity` (PyPI) | [idemity-python](https://github.com/idemity/idemity-python) |
| Go | `github.com/idemity/idemity-go` | [idemity-go](https://github.com/idemity/idemity-go) |
| Flutter / Dart | `idemity` (pub.dev) | [idemity-flutter](https://github.com/idemity/idemity-flutter) |
| Laravel / PHP | `idemity/laravel-sdk` (Packagist) | [idemity-laravel](https://github.com/idemity/idemity-laravel) |

## Quick look

```ts
import { Idemity } from 'idemity'
import fs from 'node:fs'

const idemity = new Idemity({ apiKey: 'idm_live_…' })

// 1:N search — who is this?
const { matches } = await idemity.faces.identify('col_employees', {
  image: fs.readFileSync('./photo.jpg'),
  top_k: 3,
})

for (const m of matches) {
  console.log(`${m.externalId} — ${(m.confidence * 100).toFixed(1)}%`)
}
```

## Run it where you need it

- **Cloud** — hosted at `api.idemity.com`; start with a key, no infrastructure to manage.
- **On-prem & air-gapped** — the same images run inside your network with a signed license, for teams that can't send faces to a third party.

---

<p align="center">
  <sub>Idemity · face recognition API · <a href="https://idemity.com">idemity.com</a></sub>
</p>
