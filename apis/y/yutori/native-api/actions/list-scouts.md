# List Scouts with Yutori

Retrieves scouting tasks for the current Yutori account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scouting/tasks`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [List Scouts](https://docs.yutori.com/reference/scouts-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional scout status filter. |
| `include_all_sources` | query | `boolean` | no | Whether to include all source types. |
| `page_size` | query | `number` | no | Maximum number of scouts to return. |
| `cursor` | query | `string` | no | Cursor for the next page of scouts. |
