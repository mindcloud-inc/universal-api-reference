# Start Classification Job From URL with Mindee

Creates a new classification job in Mindee from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/products/classification/enqueue`
- **Base URL:** `https://api-v2.mindee.net`
- **Official documentation:** [Start Classification Job From URL](https://docs.mindee.com/integrations/api-reference/classification-models)

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
