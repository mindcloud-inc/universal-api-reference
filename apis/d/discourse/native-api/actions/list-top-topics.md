# List Top Topics with Discourse

Retrieves top Discourse topics for a selected period.

## Endpoint

- **Method:** `GET`
- **Path:** `/top.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [List Top Topics](https://docs.discourse.org/#tag/Topics/operation/listTopTopics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `period` | query | `string` | no | Time period used to filter top topics. |
