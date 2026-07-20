# Create Access Token with Scalr

Creates a new access token in Scalr.

## Endpoint

- **Method:** `POST`
- **Path:** `/access-tokens`
- **Base URL:** `https://mindcloud.scalr.io/api/iacp/v3`
- **Official documentation:** [Create Access Token](https://docs.scalr.io/reference/create_access_token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | no | Access token name. |
| `data.attributes.description` | body | `string` | no | Access token description. |
| `data.attributes.expires-in` | body | `number` | no | Minutes until the token expires. |
