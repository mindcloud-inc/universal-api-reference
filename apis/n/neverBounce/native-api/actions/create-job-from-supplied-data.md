# Create Job From Supplied Data with NeverBounce

Creates a verification job in NeverBounce from supplied rows.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/create`
- **Base URL:** `https://api.neverbounce.com/v4.2`
- **Official documentation:** [Create Job From Supplied Data](https://developers.neverbounce.com/reference/jobs-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input[]` | body | `array<object>` | yes | Supplied rows to verify. |
| `input[].email` | body | `string` | yes | Email address for the supplied row. |
| `input[].name` | body | `string` | no | Optional name or label to store with the supplied row. |
| `auto_parse` | body | `boolean` | no | Parse the job immediately after creation. |
| `auto_start` | body | `boolean` | no | Start the job immediately after it is parsed. |
| `run_sample` | body | `boolean` | no | Run the provider sample mode before processing the full job. |
| `filename` | body | `string` | no | Display filename for the supplied job. |
| `allow_manual_review` | body | `boolean` | no | Allow manual review for unresolved rows. |
| `callback_url` | body | `string` | no | Webhook URL for job updates. |
| `callback_headers` | body | `object` | no | Optional headers to send with the callback request. |
| `request_meta_data.leverage_historical_data` | body | `number` | no | Set to 1 to enable NeverBounce historical-data leverage for this job. |
