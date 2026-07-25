# Activate a user with Weaviate Vector Store

Activates a user in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/db/:user_id/activate`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Activate a user](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userid` | path | `string` | yes | The name of the user. |
