# List Aggregated Campaign Statistics with Vouchery.io

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/aggregated_statistics`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [List Aggregated Campaign Statistics](https://docs.vouchery.io/reference/getapiv21campaignsaggregatedstatistics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | query | `number` | no | Optional campaign ID to narrow aggregated statistics. |
| `range` | query | `number` | no | Statistics range in days. Default 30, max 90. |
