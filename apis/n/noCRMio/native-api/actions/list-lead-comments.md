# List Lead Comments with noCRM.io

Retrieves lead comments from noCRM.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads/:lead_id/comments`
- **Base URL:** `{baseUrl}/api/v2`
- **Official documentation:** [List Lead Comments](https://www.nocrm.io/api#retrieve-all-comments-from-a-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `string` | yes | Lead ID. |
| `direction` | query | `string` | no | Sort direction for returned comments. |
