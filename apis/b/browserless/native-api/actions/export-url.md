# Export Url with Browserless

Downloads a URL in its native format from Browserless.

## Endpoint

- **Method:** `POST`
- **Path:** `/export`
- **Base URL:** `https://production-sfo.browserless.io`
- **Official documentation:** [Export Url](https://docs.browserless.io/rest-apis/export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL to export in its native content type. |
| `includeResources` | body | `boolean` | no | Whether to return a ZIP archive with the page HTML and linked resources. |
