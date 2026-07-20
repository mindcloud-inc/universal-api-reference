# BackgroundCut: Native API Reference

A consolidated summary of BackgroundCut's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://backgroundcut.co/api/
- **API base URL:** `https://backgroundcut.co/api/v1/`

## Authentication

### API Key

Provide your BackgroundCut API key. This app sends it exactly as the provider requires: `Authorization: Token <apiKey>` for v1 actions and raw `Authorization: <apiKey>` for v2 actions.

### Credentials

- **API Key:** `apiKey` · required · Your BackgroundCut API key. MindCloud stores this as the single secret source of truth and injects it with the exact header shape each action requires.

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://backgroundcut.co/api/)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Alpha Mask From Base64 (v2)](actions/generate-alpha-mask-from-base64-v2.md) | `POST https://api.backgroundcut.co/v2/cut/` | [docs](https://backgroundcut.co/api/docs/v2/) |
| [Generate Alpha Mask From File (v2)](actions/generate-alpha-mask-from-file-v2.md) | `POST https://api.backgroundcut.co/v2/cut/` | [docs](https://backgroundcut.co/api/docs/v2/) |
| [Remove Background From Base64 (v2)](actions/remove-background-from-base64-v2.md) | `POST https://api.backgroundcut.co/v2/cut/` | [docs](https://backgroundcut.co/api/docs/v2/) |
| [Remove Background From File (v1)](actions/remove-background-from-file-v1.md) | `POST cut/` | [docs](https://backgroundcut.co/api/docs/v1/) |
| [Remove Background From File (v2)](actions/remove-background-from-file-v2.md) | `POST https://api.backgroundcut.co/v2/cut/` | [docs](https://backgroundcut.co/api/docs/v2/) |
| [Remove Background From Image URL (v1)](actions/remove-background-from-image-url-v1.md) | `POST cut/` | [docs](https://backgroundcut.co/api/docs/v1/) |
