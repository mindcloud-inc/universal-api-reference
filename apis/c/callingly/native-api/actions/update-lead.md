# Update Lead with Callingly

Updates a lead in Callingly.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/leads/{{id}}`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [Update Lead](https://help.callingly.com/article/38-callingly-api-documentation#Update-Agent-sx_cL)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | The lead company. |
| `email` | body | `string` | no | The lead email address. |
| `fname` | body | `string` | no | The lead first name. |
| `id` | path | `number` | yes | The Callingly lead ID to update. |
| `id` | body | `number` | yes | The lead ID in the request body, as shown in the docs sample. |
| `is_blocked` | body | `number` | no | Whether the lead is blocked. |
| `is_stopped` | body | `number` | no | Whether the lead is stopped. |
| `lname` | body | `string` | no | The lead last name. |
| `phone_number` | body | `string` | no | The lead phone number. |
| `result` | body | `string` | no | The lead result. |
| `source` | body | `string` | no | The lead source. |
| `stage` | body | `string` | no | The lead stage. |
| `status` | body | `string` | no | The lead status. |
