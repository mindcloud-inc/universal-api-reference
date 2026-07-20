# List Group Receivers with CleverReach

Retrieves receivers for a group in CleverReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/groups.json/:groupId/receivers`
- **Base URL:** `https://rest.cleverreach.com`
- **Official documentation:** [List Group Receivers](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `string` | yes | Group ID. |
| `pagesize` | query | `number` | no | Pagesize (max 5000). |
| `page` | query | `number` | no | Page (zero-based). |
| `type` | query | `string` | no | Type. Accepted values: `0`, `1`, `2`, `3`. |
| `detail` | query | `number` | no | Detail depth (bitwise combinable) (0: none, 1: events, 2: orders, 4: tags). |
| `email_list` | query | `string` | no | list of receiver emails to filter for. Comma separated like: "foo@bar.com,bar@foo.com,...". |
| `id_list` | query | `string` | no | list of Receiver ID's to filter for. comma separated like: "123,633,5342". |
| `order_by` | query | `string` | no | field to order by, append 'asc' or 'desc' with a space. |
