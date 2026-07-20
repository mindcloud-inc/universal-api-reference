# Create Schedule with Olostep

Creates a new schedule in Olostep.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/schedules`
- **Base URL:** `https://api.olostep.com`
- **Official documentation:** [Create Schedule](https://docs.olostep.com/api-reference/schedules/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `method` | body | `string` | yes | HTTP method the schedule should use when calling the Olostep endpoint. Accepted values: `0`, `1`. |
| `endpoint` | body | `string` | yes | Olostep API endpoint path to call, such as `/v1/retrieve` or `/v1/searches`. |
| `payload` | body | `object` | no | JSON payload to send when the scheduled request runs. |
| `cron_expression` | body | `string` | no | Cron expression for a recurring schedule. |
| `execute_at` | body | `date` | no | One-time execution timestamp in ISO 8601 format. |
| `expression_timezone` | body | `string` | no | Timezone used when interpreting the cron expression. |
| `text` | body | `string` | no | Natural-language schedule text for Olostep to interpret. |
