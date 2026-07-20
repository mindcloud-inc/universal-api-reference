# Create Access Token with Testlify

Creates a new access token in Testlify.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/workspace/accesstoken/generate`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [Create Access Token](https://docs.testlify.com/reference/generate_access_token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `note` | body | `string` | no | Descriptive note for the access token. |
| `expiration` | body | `date` | no | Token expiration timestamp in ISO 8601 format. |
