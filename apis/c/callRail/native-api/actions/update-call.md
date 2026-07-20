# Update Call with CallRail

Updates a call in CallRail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/a/:account_id/calls/:call_id.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Update Call](https://apidocs.callrail.com/#updating-a-call)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `call_id` | path | `string` | yes |
| `tags[]` | body | `array<string>` | no |
| `append_tags` | body | `boolean` | no |
| `lead_status` | body | `string` | no |
| `value` | body | `string` | no |
| `note` | body | `string` | no |
| `customer_name` | body | `string` | no |
| `spam` | body | `boolean` | no |
