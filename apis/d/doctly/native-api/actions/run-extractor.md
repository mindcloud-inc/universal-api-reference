# Run Extractor with Doctly

## Endpoint

- **Method:** `POST`
- **Path:** `/e/:slug`
- **Base URL:** `https://api.doctly.ai/api/v1`
- **Official documentation:** [Run Extractor](https://docs.doctly.ai/api-reference/extractors/run)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Extractor slug to execute, such as invoice-extractor. |
| `file` | body | `file` | yes | Document file to process. Provide either file or URL. |
| `callback_url` | body | `string` | no | HTTPS webhook URL to notify when extraction completes. |
