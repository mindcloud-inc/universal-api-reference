# Stable Diffusion: Native API Reference

A consolidated summary of Stable Diffusion's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://platform.stability.ai/docs/api-reference
- **API base URL:** `https://api.stability.ai`

## Authentication

### API Key

Authenticate with a Stability AI API key sent as an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://platform.stability.ai/docs/api-reference)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Control Sketch Image](actions/control-sketch-image.md) | `POST /v2beta/stable-image/control/sketch` | [docs](https://platform.stability.ai/docs/api-reference#tag/Control/paths/~1v2beta~1stable-image~1control~1sketch/post) |
| [Control Structure Image](actions/control-structure-image.md) | `POST /v2beta/stable-image/control/structure` | [docs](https://platform.stability.ai/docs/api-reference#tag/Control/paths/~1v2beta~1stable-image~1control~1structure/post) |
| [Control Style Image](actions/control-style-image.md) | `POST /v2beta/stable-image/control/style` | [docs](https://platform.stability.ai/docs/api-reference#tag/Control/paths/~1v2beta~1stable-image~1control~1style/post) |
| [Erase Image Region](actions/erase-image-region.md) | `POST /v2beta/stable-image/edit/erase` | [docs](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1erase/post) |
| [Generate Audio From Text](actions/generate-audio-from-text.md) | `POST /v2beta/audio/stable-audio-2/text-to-audio` | [docs](https://platform.stability.ai/docs/api-reference#tag/Stable%20Audio%202/paths/~1v2beta~1audio~1stable-audio-2~1text-to-audio/post) |
| [Generate Core Image](actions/generate-core-image.md) | `POST /v2beta/stable-image/generate/core` | [docs](https://platform.stability.ai/docs/api-reference#tag/Generate/paths/~1v2beta~1stable-image~1generate~1core/post) |
| [Generate SD3 Image](actions/generate-sd3-image.md) | `POST /v2beta/stable-image/generate/sd3` | [docs](https://platform.stability.ai/docs/api-reference#tag/Generate/paths/~1v2beta~1stable-image~1generate~1sd3/post) |
| [Generate Ultra Image](actions/generate-ultra-image.md) | `POST /v2beta/stable-image/generate/ultra` | [docs](https://platform.stability.ai/docs/api-reference#tag/Generate/paths/~1v2beta~1stable-image~1generate~1ultra/post) |
| [Generate XL Image](actions/generate-xl-image.md) | `POST /v1/generation/stable-diffusion-xl-1024-v1-0/text-to-image` | [docs](https://staging-api.stability.ai/docs) |
| [Get Account](actions/get-account.md) | `GET /v1/user/account` | [docs](https://staging-api.stability.ai/docs) |
| [Get Async Upscale Result](actions/get-async-upscale-result.md) | `GET /v2alpha/generation/stable-image/upscale/result/{id}` | [docs](https://platform.stability.ai/docs/api-reference#tag/v2alpha%2Fgeneration/paths/~1v2alpha~1generation~1stable-image~1upscale~1result~1{id}/get) |
| [Get Balance](actions/get-balance.md) | `GET /v1/user/balance` | [docs](https://staging-api.stability.ai/docs) |
| [Get Creative Upscale Result](actions/get-creative-upscale-result.md) | `GET /v2beta/stable-image/upscale/creative/result/{id}` | [docs](https://platform.stability.ai/docs/api-reference#tag/Results/paths/~1v2beta~1stable-image~1upscale~1creative~1result~1{id}/get) |
| [Get Generation Result](actions/get-generation-result.md) | `GET /v2beta/results/{id}` | [docs](https://platform.stability.ai/docs/api-reference#tag/Results/paths/~1v2beta~1results~1{id}/get) |
| [Inpaint Audio](actions/inpaint-audio.md) | `POST /v2beta/audio/stable-audio-2/inpaint` | [docs](https://platform.stability.ai/docs/api-reference#tag/Stable%20Audio%202/paths/~1v2beta~1audio~1stable-audio-2~1inpaint/post) |
| [Inpaint Image](actions/inpaint-image.md) | `POST /v2beta/stable-image/edit/inpaint` | [docs](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1inpaint/post) |
| [Inpaint Legacy Image](actions/inpaint-legacy-image.md) | `POST /v2alpha/generation/stable-image/inpaint` | [docs](https://platform.stability.ai/docs/api-reference#tag/v2alpha%2Fgeneration/paths/~1v2alpha~1generation~1stable-image~1inpaint/post) |
| [List Engines](actions/list-engines.md) | `GET /v1/engines/list` | [docs](https://staging-api.stability.ai/docs) |
| [Mask XL Image](actions/mask-xl-image.md) | `POST /v1/generation/stable-diffusion-xl-1024-v1-0/image-to-image/masking` | [docs](https://staging-api.stability.ai/docs) |
| [Outpaint Image](actions/outpaint-image.md) | `POST /v2beta/stable-image/edit/outpaint` | [docs](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1outpaint/post) |
| [Remove Background](actions/remove-background.md) | `POST /v2beta/stable-image/edit/remove-background` | [docs](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1remove-background/post) |
| [Replace Background And Relight](actions/replace-background-and-relight.md) | `POST /v2beta/stable-image/edit/replace-background-and-relight` | [docs](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1replace-background-and-relight/post) |
| [Search And Recolor](actions/search-and-recolor.md) | `POST /v2beta/stable-image/edit/search-and-recolor` | [docs](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1search-and-recolor/post) |
| [Search And Replace](actions/search-and-replace.md) | `POST /v2beta/stable-image/edit/search-and-replace` | [docs](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1search-and-replace/post) |
| [Submit Async Upscale](actions/submit-async-upscale.md) | `POST /v2alpha/generation/stable-image/upscale` | [docs](https://platform.stability.ai/docs/api-reference#tag/v2alpha%2Fgeneration/paths/~1v2alpha~1generation~1stable-image~1upscale/post) |
| [Transfer Style Image](actions/transfer-style-image.md) | `POST /v2beta/stable-image/control/style-transfer` | [docs](https://platform.stability.ai/docs/api-reference#tag/Control/paths/~1v2beta~1stable-image~1control~1style-transfer/post) |
| [Transform Audio From Audio](actions/transform-audio-from-audio.md) | `POST /v2beta/audio/stable-audio-2/audio-to-audio` | [docs](https://platform.stability.ai/docs/api-reference#tag/Stable%20Audio%202/paths/~1v2beta~1audio~1stable-audio-2~1audio-to-audio/post) |
| [Transform XL Image](actions/transform-xl-image.md) | `POST /v1/generation/stable-diffusion-xl-1024-v1-0/image-to-image` | [docs](https://staging-api.stability.ai/docs) |
| [Upscale Image Conservative](actions/upscale-image-conservative.md) | `POST /v2beta/stable-image/upscale/conservative` | [docs](https://platform.stability.ai/docs/api-reference#tag/Upscale/paths/~1v2beta~1stable-image~1upscale~1conservative/post) |
| [Upscale Image Creative](actions/upscale-image-creative.md) | `POST /v2beta/stable-image/upscale/creative` | [docs](https://platform.stability.ai/docs/api-reference#tag/Upscale/paths/~1v2beta~1stable-image~1upscale~1creative/post) |
| [Upscale Image Fast](actions/upscale-image-fast.md) | `POST /v2beta/stable-image/upscale/fast` | [docs](https://platform.stability.ai/docs/api-reference#tag/Upscale/paths/~1v2beta~1stable-image~1upscale~1fast/post) |
