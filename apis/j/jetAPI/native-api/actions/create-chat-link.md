# Create Chat Link with JetAPI

Creates a new chat link in JetAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/chatter/`
- **Base URL:** `https://api.jetapi.io`
- **Official documentation:** [Create Chat Link](https://docs.jetapi.io/#df8a4c17-418b-41f8-b3ad-fbb018210e1a)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_type` | query | `number` | no | 0 requires password entry, 1 disables password entry. |
| `password` | query | `string` | no | Password for logging into iframe chat when auth_type=0. |
