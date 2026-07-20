# Update Access Token with Scalr

Updates an existing access token in Scalr.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/access-tokens/:access_token`
- **Base URL:** `https://mindcloud.scalr.io/api/iacp/v3`
- **Official documentation:** [Update Access Token](https://docs.scalr.io/reference/update_access_token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_token` | path | `string` | yes | Scalr access token ID. |
| `data.attributes.name` | body | `string` | no | Access token name. |
| `data.attributes.description` | body | `string` | no | Access token description. |
| `data.attributes.expires-in` | body | `number` | no | Minutes until the token expires. |
