# Update Campaign with CueGrowth

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaigns/{campaign_id}/update`
- **Base URL:** `https://api.cuegrowth.ai/public/api`
- **Official documentation:** [Update Campaign](https://cuegrowth.ai/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | ID of the campaign. |
| `message_active` | body | `boolean` | no | Whether the invite or first message is active. |
| `followup_active` | body | `boolean` | no | Whether the first follow-up is active. |
| `second_followup_active` | body | `boolean` | no | Whether the second follow-up is active. |
| `third_followup_active` | body | `boolean` | no | Whether the third follow-up is active. |
