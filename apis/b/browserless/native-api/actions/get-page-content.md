# Get Page Content with Browserless

Retrieves rendered page content from Browserless.

## Endpoint

- **Method:** `POST`
- **Path:** `/content`
- **Base URL:** `https://production-sfo.browserless.io`
- **Official documentation:** [Get Page Content](https://docs.browserless.io/rest-apis/content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL to render and return as HTML content. |
