# Get User with Damstra Forms

Retrieves a user from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/{id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get User](https://sammapi.docs.apiary.io/#reference/users/user-instance/retrieve-a-user)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique id (numeric) or uuid (string) of the user. |
| `show_managed` | query | `boolean` | no | Show/hide the managed attribute. |
