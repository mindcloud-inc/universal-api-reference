# Dynamic Mockups: Native API Reference

A consolidated summary of Dynamic Mockups's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.dynamicmockups.com
- **API base URL:** `https://app.dynamicmockups.com`

## Authentication

### API Key

Use your Dynamic Mockups API key in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.dynamicmockups.com/getting-started/how-can-i-get-my-api-key)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bulk Renders](actions/create-bulk-renders.md) | `POST api/v1/renders/bulk` | [docs](https://docs.dynamicmockups.com/api-reference/bulk-render-mockups-api) |
| [Create Collection](actions/create-collection.md) | `POST api/v1/collections` | [docs](https://docs.dynamicmockups.com/api-reference/get-collections-api) |
| [Create Mockup Render](actions/create-mockup-render.md) | `POST api/v1/renders` | [docs](https://docs.dynamicmockups.com/api-reference/render-api) |
| [Delete PSD File](actions/delete-psd-file.md) | `POST api/v1/psd/delete` | [docs](https://docs.dynamicmockups.com/api-reference/psd-upload-api) |
| [Export Print Files](actions/export-print-files.md) | `POST api/v1/renders/print-files` | [docs](https://docs.dynamicmockups.com/api-reference/render-print-files-api) |
| [Get Mockup](actions/get-mockup.md) | `GET api/v1/mockup/:uuid` | [docs](https://docs.dynamicmockups.com/api-reference/get-mockups-api) |
| [List Catalogs](actions/list-catalogs.md) | `GET api/v1/catalogs` | [docs](https://docs.dynamicmockups.com/api-reference/catalogs-api) |
| [List Collections](actions/list-collections.md) | `GET api/v1/collections` | [docs](https://docs.dynamicmockups.com/api-reference/get-collections-api) |
| [List Mockups](actions/list-mockups.md) | `GET api/v1/mockups` | [docs](https://docs.dynamicmockups.com/api-reference/get-mockups-api) |
| [Render Multiple Mockups](actions/render-multiple-mockups.md) | `POST api/v1/renders/batch` | [docs](https://docs.dynamicmockups.com/api-reference/batch-render-mockups-api) |
| [Upload PSD File](actions/upload-psd-file.md) | `POST api/v1/psd/upload` | [docs](https://docs.dynamicmockups.com/api-reference/psd-upload-api) |
