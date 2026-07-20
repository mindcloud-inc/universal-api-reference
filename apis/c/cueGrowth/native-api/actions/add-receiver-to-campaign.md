# Add Receiver To Campaign with CueGrowth

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/add_receiver_to_campaign`
- **Base URL:** `https://api.cuegrowth.ai/public/api`
- **Official documentation:** [Add Receiver To Campaign](https://cuegrowth.ai/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `number` | yes | ID of the CSV campaign. |
| `linkedin_url` | body | `string` | yes | LinkedIn URL of the receiver. |
| `email` | body | `string` | no | Email of the receiver. |
| `external_id` | body | `string` | no | External CRM ID of the receiver. |
| `custom_followups[]` | body | `array<object>` | no | Specific follow-up messages to send to this receiver. |
