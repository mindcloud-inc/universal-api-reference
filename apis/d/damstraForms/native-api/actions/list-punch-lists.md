# List Punch Lists with Damstra Forms

Retrieves punch lists from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/punch_lists`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Punch Lists](https://sammapi.docs.apiary.io/#reference/punch-lists/punch-list-collection/get-a-list-of-punch-lists)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Only return forms associate with the specified project. |
| `status` | query | `string` | no | Statuses to include in returned results. You can combine statuses by separating them with "\|" (e.g. draft\|open, open\|closed, etc.) Accepted values: `0`, `1`, `2`. Send multiple values as a string separated by `\|`. |
| `updated_from` | query | `string` | no | Only return results updated after the specified value. It will try to make sense of whatever datetime format you provide, but the example shows the officially supported format. |
