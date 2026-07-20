# List Push Messages with Countly

Retrieves all push messages from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o/pushes/all`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [List Push Messages](https://api.count.ly/reference/opushes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to list push messages for. |
| `source` | query | `string` | no | Push source filter, such as api or dash. |
| `sSearch` | query | `string` | no | Search text for the default message. |
| `iDisplayStart` | query | `number` | no | Number of push records to skip. |
| `iDisplayLength` | query | `number` | no | Number of push records to return. |
| `iSortCol_0` | query | `string` | no | Column to sort push messages by. |
| `sSortDir_0` | query | `string` | no | Sort direction, asc or desc. |
