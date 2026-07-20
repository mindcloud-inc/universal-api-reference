# Get User with Crexendo

Retrieves a user from Crexendo.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/:domain/users/:user`
- **Base URL:** `https://ns-api.com/ns-api/v2`
- **Official documentation:** [Get User](https://docs.ns-api.com/reference/getuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain identifier, for example apps.mindcloud.co. |
| `user` | path | `string` | yes | User extension or identifier, for example 1000. |
