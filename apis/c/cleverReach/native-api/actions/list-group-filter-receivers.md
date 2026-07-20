# List Group Filter Receivers with CleverReach

Retrieves group filter receivers from CleverReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/groups.json/:groupId/filters/:filterId/receivers`
- **Base URL:** `https://rest.cleverreach.com`
- **Official documentation:** [List Group Filter Receivers](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `string` | yes | Group ID. |
| `filter_id` | path | `string` | yes | Filter ID. |
| `pagesize` | query | `number` | no | Pagesize (max 5000). |
| `page` | query | `number` | no | Page (zero-based). |
| `type` | query | `string` | no | Type. Accepted values: `0`, `1`, `2`, `3`. |
| `detail` | query | `number` | no | Detail depth (bitwise combinable) (0: none, 1: events, 2: orders, 4: tags). |
| `email_list` | query | `string` | no | list of Receiver Emails's to filter for. comma separated like: "foo@bar.com,bar@foo.com,...". |
| `id_list` | query | `string` | no | list of Receiver ID's to filter for. comma separated like: "123,633,5342". |
| `order_by` | query | `string` | no | field to order by, append 'asc' or 'desc' with a space. |
