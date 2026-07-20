# Start Extraction Job From URL with Mindee

Creates a new extraction job in Mindee from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/products/extraction/enqueue`
- **Base URL:** `https://api-v2.mindee.net`
- **Official documentation:** [Start Extraction Job From URL](https://docs.mindee.com/integrations/api-reference/extraction-models)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_id` | body | `string` | yes | Model ID to use for the inference. |
| `url` | body | `string` | yes | Download the file from a public HTTPS URL. |
