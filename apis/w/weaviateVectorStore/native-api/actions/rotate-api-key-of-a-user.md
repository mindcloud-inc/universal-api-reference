# Rotate API key of a user with Weaviate Vector Store

Rotates API key of a user in Weaviate.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/db/:user_id/rotate-key`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Rotate API key of a user](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userid` | path | `string` | yes | The name of the user. |
