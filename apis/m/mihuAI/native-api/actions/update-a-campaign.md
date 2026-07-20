# Update a Campaign with Mihu AI

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/campaigns/:uuid`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Update a Campaign](https://developers.mihu.ai/api-reference/campaigns/update-a-campaign)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agent_app_id` | body | `number` | no |
| `agent_id` | body | `number` | no |
| `campaign_type` | body | `string` | no |
| `description` | body | `string` | no |
| `end_date` | body | `string` | no |
| `name` | body | `string` | no |
| `start_date` | body | `string` | no |
| `status` | body | `string` | no |
| `uuid` | path | `string` | yes |
