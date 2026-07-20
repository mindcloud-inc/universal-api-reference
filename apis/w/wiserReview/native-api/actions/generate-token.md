# Generate Token with WiserReview

Generates an auth token for WiserReview.

## Endpoint

- **Method:** `GET`
- **Path:** `/authToken`
- **Base URL:** `https://api.wiserreview.com/api/v1`
- **Official documentation:** [Generate Token](https://apidocs.wiserreview.com/generate-token-26189664e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_key` | query | `string` | yes | API key from Settings in the WiserReview dashboard. |
| `expiresIn` | query | `number` | no | Optional number of days before the generated auth token expires. |
