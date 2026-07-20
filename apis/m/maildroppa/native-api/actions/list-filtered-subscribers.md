# List Filtered Subscribers with Maildroppa

Finds Maildroppa subscribers by segment expression.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/filtered`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [List Filtered Subscribers](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filterGroups[]` | body | `array` | no | Filter groups that compose this expression. |
| `operator` | body | `string` | no | Logical operator that applies between filter groups. |
| `pageNumber` | query | `number` | no | Page number. |
| `pageSize` | query | `number` | no | Number of items per page. |
| `status` | query | `string` | no | Subscriber status filter. |
