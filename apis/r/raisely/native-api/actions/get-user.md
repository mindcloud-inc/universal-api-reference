# Get User with Raisely

Retrieves a user from Raisely.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:uuid`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [Get User](https://developers.raisely.com/reference/getuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | The `uuid` of the record |
| `private` | query | `boolean` | no | Returns the full record when authenticated |
