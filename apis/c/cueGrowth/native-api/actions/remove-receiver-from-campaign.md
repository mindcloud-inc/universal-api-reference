# Remove Receiver From Campaign with CueGrowth

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/remove_receiver_from_campaign`
- **Base URL:** `https://api.cuegrowth.ai/public/api`
- **Official documentation:** [Remove Receiver From Campaign](https://cuegrowth.ai/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `number` | yes | ID of the CSV campaign. |
| `linkedin_url` | body | `string` | yes | LinkedIn URL of the receiver. |
| `email` | body | `string` | no | Email of the receiver. |
| `external_id` | body | `string` | no | External CRM ID of the receiver. |
