# Placedog: Native API Reference

A consolidated summary of Placedog's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://placedog.net/
- **API base URL:** `https://placedog.net`

## Authentication

### No Auth

Placedog is a public URL API and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://placedog.net/)

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Blurred Placeholder Image](actions/get-blurred-placeholder-image.md) | `GET /[:width]/[:height]/b` | [docs](https://placedog.net/) |
| [Get Filtered Placeholder Image](actions/get-filtered-placeholder-image.md) | `GET /[:width]/[:height]/[:filter]` | [docs](https://placedog.net/) |
| [Get Filtered Specific Image](actions/get-filtered-specific-image.md) | `GET /[:width]/[:height]/[:filter]` | [docs](https://placedog.net/) |
| [Get Greyscale Placeholder Image](actions/get-greyscale-placeholder-image.md) | `GET /[:width]/[:height]/g` | [docs](https://placedog.net/) |
| [Get Placeholder Image](actions/get-placeholder-image.md) | `GET /[:width]` | [docs](https://placedog.net/) |
| [Get Placeholder Image By Dimensions](actions/get-placeholder-image-by-dimensions.md) | `GET /[:width]/[:height]` | [docs](https://placedog.net/) |
| [Get Placeholder Image By X Dimensions](actions/get-placeholder-image-by-x-dimensions.md) | `GET /[:width]x[:height]` | [docs](https://placedog.net/) |
| [Get Random Placeholder Image](actions/get-random-placeholder-image.md) | `GET /[:width]/[:height]` | [docs](https://placedog.net/) |
| [Get Specific Image](actions/get-specific-image.md) | `GET /[:width]/[:height]` | [docs](https://placedog.net/images) |
| [List Images](actions/list-images.md) | `GET /images` | [docs](https://placedog.net/images) |
