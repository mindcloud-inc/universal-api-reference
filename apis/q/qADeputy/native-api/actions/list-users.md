# List Users with QADeputy

Retrieves users from QADeputy.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [List Users](https://apidocs.qadeputy.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_status` | query | `list` | no | Optional user status filter. The API defaults to active. Accepted values: `0`, `1`. |
| `sort_field` | query | `list` | no | Optional field to sort users by: role, first_name, or last_name. Accepted values: `0`, `1`, `2`. |
| `sort_type` | query | `list` | no | Optional user sort direction: asc or desc. Accepted values: `0`, `1`. |
