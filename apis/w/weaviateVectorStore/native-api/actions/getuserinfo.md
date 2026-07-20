# Get user info with Weaviate Vector Store

Retrieves user info from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/db/:user_id`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get user info](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The name of the user. |
| `includeLastUsedTime` | query | `string` | no | Whether to include the last used time of the given user |
