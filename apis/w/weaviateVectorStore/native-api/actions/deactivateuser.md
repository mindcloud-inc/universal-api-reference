# Deactivate a user with Weaviate Vector Store

Deactivates a user in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/db/:user_id/deactivate`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Deactivate a user](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The name of the user. |
