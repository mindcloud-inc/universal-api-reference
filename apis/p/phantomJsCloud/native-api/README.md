# PhantomJsCloud: Native API Reference

A consolidated summary of PhantomJsCloud's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://phantomjscloud.com/docs/http-api/
- **API base URL:** `https://phantomjscloud.com/api/browser/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://phantomjscloud.com/docs/http-api/)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Capture Screenshot as JPEG](actions/capture-screenshot-as-jpeg.md) | `POST /:apiKey/` | [docs](https://phantomjscloud.com/docs/http-api/) |
| [Capture Screenshot as PNG](actions/capture-screenshot-as-png.md) | `POST /:apiKey/` | [docs](https://phantomjscloud.com/docs/http-api/) |
| [Render Page as HTML](actions/render-page-as-html.md) | `POST /:apiKey/` | [docs](https://phantomjscloud.com/docs/http-api/) |
| [Render Page as PDF](actions/render-page-as-pdf.md) | `POST /:apiKey/` | [docs](https://phantomjscloud.com/docs/http-api/) |
| [Render Page as Text](actions/render-page-as-text.md) | `POST /:apiKey/` | [docs](https://phantomjscloud.com/docs/http-api/) |
| [Run Browser Automation](actions/run-browser-automation.md) | `POST /:apiKey/` | [docs](https://phantomjscloud.com/docs/http-api/automation/) |
