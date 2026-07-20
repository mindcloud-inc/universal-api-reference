# List Groups with Userflow

Retrieves a list of groups from Userflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups`
- **Base URL:** `https://api.userflow.com`
- **Official documentation:** [List Groups](https://docs.userflow.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of groups to return. |
| `starting_after` | query | `string` | no | Return groups after this group ID. |
| `order_by` | query | `string` | no | Sort groups by one or more supported fields. |
