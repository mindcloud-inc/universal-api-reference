# Update User Type with Engage

Converts a user between customer and account in Engage.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:uid/convert`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Update User Type](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#change-user-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | The entity type to convert to: customer or account. |
| `uid` | path | `string` | yes | The user ID from your application. |
