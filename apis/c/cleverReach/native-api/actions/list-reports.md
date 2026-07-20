# List Reports with CleverReach

Retrieves reports from your CleverReach account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/reports.json`
- **Base URL:** `https://rest.cleverreach.com`
- **Official documentation:** [List Reports](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/reports-v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pagesize` | query | `number` | no | max items. |
| `page` | query | `number` | no | page. |
| `channel_id` | query | `string` | no | optional: if specified, it will only return matching results. |
| `start` | query | `number` | no | start date (unix timestamp), requires end date. |
| `end` | query | `number` | no | end date (unix timestamp), requires start date. |
| `group_id` | query | `string` | no | get only reports for this group ID. |
