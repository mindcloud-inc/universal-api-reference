# Create Job From Remote URL with NeverBounce

Creates a verification job in NeverBounce from a remote CSV URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/create`
- **Base URL:** `https://api.neverbounce.com/v4.2`
- **Official documentation:** [Create Job From Remote URL](https://developers.neverbounce.com/reference/jobs-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auto_parse` | body | `boolean` | no | Parse the job automatically after creation. |
| `input` | body | `string` | yes | Remote CSV URL for NeverBounce to import. |
| `auto_start` | body | `boolean` | no | Start the job automatically after parsing completes. |
| `run_sample` | body | `boolean` | no | Run the sample flow before processing the full job. |
| `filename` | body | `string` | no | Filename to associate with the job. |
| `allow_manual_review` | body | `boolean` | no | Allow NeverBounce manual review for this job. |
| `callback_url` | body | `string` | no | Webhook URL NeverBounce should call after job events. |
| `callback_headers` | body | `object` | no | Optional headers to send with the callback request. |
| `request_meta_data.leverage_historical_data` | body | `number` | no | Set to 1 to enable NeverBounce historical-data leverage for this job. |
