# List Users with Damstra Forms

Retrieves users from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Users](https://sammapi.docs.apiary.io/#reference/users/user-collection/get-a-list-of-users)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `string` | no | Active state (true = Active, false = Inactive, all = All). Accepted values: `0`, `1`, `2`. |
| `updated_from` | query | `string` | no | Only return results updated after the specified value. It will try to make sense of whatever datetime format you provide, but the example shows the officially supported format. |
| `show_managed` | query | `boolean` | no | Show/hide the managed attribute. |
