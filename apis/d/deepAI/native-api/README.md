# DeepAI: Native API Reference

A consolidated summary of DeepAI's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://api.deepai.org/docs
- **API base URL:** `https://api.deepai.org/api`

## Authentication

### API Key

Authenticate with a DeepAI API key from the DeepAI profile page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
api-key: <apiKey>
```

[Official authentication documentation](https://api.deepai.org/docs)

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Colorize Image](actions/colorize-image.md) | `POST /colorizer` | [docs](https://api.deepai.org/docs) |
| [Creative Upscale](actions/creative-upscale.md) | `POST /creative-upscale` | [docs](https://api.deepai.org/docs) |
| [Edit Image](actions/edit-image.md) | `POST /image-editor` | [docs](https://api.deepai.org/docs) |
| [Expand Image](actions/expand-image.md) | `POST /zoom-out` | [docs](https://api.deepai.org/docs) |
| [Generate Image](actions/generate-image.md) | `POST /text2img` | [docs](https://api.deepai.org/docs) |
| [Remove Background](actions/remove-background.md) | `POST /background-remover` | [docs](https://api.deepai.org/docs) |
| [Replace Image Region](actions/replace-image-region.md) | `POST /image-replace` | [docs](https://api.deepai.org/docs) |
| [Upscale Anime Image](actions/upscale-anime-image.md) | `POST /waifu2x` | [docs](https://api.deepai.org/docs) |
| [Upscale Image](actions/upscale-image.md) | `POST /torch-srgan` | [docs](https://api.deepai.org/docs) |
