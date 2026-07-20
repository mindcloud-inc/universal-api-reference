# Create An Embed Token with Felt

Creates a short-lived embed token in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/embed_token`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Create An Embed Token](https://developers.felt.com/rest-api/api-reference/embed-tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map. |
| `user_email` | query | `string` | yes | The workspace member email that will use the embed token. |
