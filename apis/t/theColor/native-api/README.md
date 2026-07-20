# The Color: Native API Reference

A consolidated summary of The Color's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://www.thecolorapi.com/docs
- **API base URL:** `https://www.thecolorapi.com`

## Authentication

### No authentication

The Color API is open to all and does not require API keys or account credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.thecolorapi.com/about)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Color Scheme By CMYK](actions/generate-color-scheme-by-cmyk.md) | `GET /scheme` | [docs](https://www.thecolorapi.com/docs) |
| [Generate Color Scheme By Hex](actions/generate-color-scheme-by-hex.md) | `GET /scheme` | [docs](https://www.thecolorapi.com/docs) |
| [Generate Color Scheme By HSL](actions/generate-color-scheme-by-hsl.md) | `GET /scheme` | [docs](https://www.thecolorapi.com/docs) |
| [Generate Color Scheme By RGB](actions/generate-color-scheme-by-rgb.md) | `GET /scheme` | [docs](https://www.thecolorapi.com/docs) |
| [Identify Color By CMYK](actions/identify-color-by-cmyk.md) | `GET /id` | [docs](https://www.thecolorapi.com/docs) |
| [Identify Color By Hex](actions/identify-color-by-hex.md) | `GET /id` | [docs](https://www.thecolorapi.com/docs) |
| [Identify Color By HSL](actions/identify-color-by-hsl.md) | `GET /id` | [docs](https://www.thecolorapi.com/docs) |
| [Identify Color By RGB](actions/identify-color-by-rgb.md) | `GET /id` | [docs](https://www.thecolorapi.com/docs) |
