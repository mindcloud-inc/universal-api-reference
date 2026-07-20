# Upload Campaign Contact List with Ringg AI

Uploads a campaign contact list to Ringg AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign/save`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Upload Campaign Contact List](https://docs.ringg.ai/api-reference/endpoint/campaign/upload-campaign-contact-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables_map` | body | `string` | yes | (Required) JSON string mapping variable names to columns |
| `agent_id` | body | `string` | yes | (Required) Unique identifier for the agent |
| `call_config` | body | `string` | yes | (Required) JSON string of call configuration |
| `country_code` | body | `string` | yes | (Required) Phone number country code (e.g., +91 for India, +1 for US) |
| `campaign_start_time` | body | `string` | yes | (Required) Start time for the campaign (DD/MM/YYYY, HH:MM format) |
| `campaign_end_time` | body | `string` | yes | (Required) End time for the campaign (DD/MM/YYYY, HH:MM format) |
| `campaign_name` | body | `string` | yes | (Required) Name of the campaign. |
| `file` | body | `string` | yes | (Required) CSV file containing the contact list. |
| `remove_invalid_rows` | body | `boolean` | no | (Optional) Auto-remove invalid rows from CSV |
| `transliterate_callee_name` | body | `boolean` | no | (Optional) Transliterate callee names to the agent's language |
