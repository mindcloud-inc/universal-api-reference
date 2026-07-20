# List Users with Sisense

Retrieves users from a Sisense instance.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/users`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [List Users](https://developer.sisense.com/guides/restApi/using-rest-api.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-delimited list of user fields to include or exclude. |
| `expand` | query | `string` | no | Expand related fields such as groups into full entities. |
