# Count Job DVU Usage with Datastreamer

Retrieves DVU usage for jobs from Datastreamer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/customer-usage/jobs`
- **Base URL:** `https://api.platform.datastreamer.io`
- **Official documentation:** [Count Job DVU Usage](https://docs.datastreamer.io/docs/jobs-dvu-count-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_ids[]` | body | `array<string>` | yes | Job IDs to include in the DVU usage count. |
| `group_by` | body | `string` | no | Optional grouping mode, for example DataSource. |
