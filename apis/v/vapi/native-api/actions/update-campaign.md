# Update Campaign with Vapi

Updates an existing campaign in Vapi.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/campaign/:id`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [Update Campaign](https://docs.vapi.ai/api-reference/campaigns/campaign-controller-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | This is the name of the campaign. This is just for your own reference. |
| `assistantId` | body | `string` | no | This is the assistant ID that will be used for the campaign calls. Can only be updated if campaign is not in progress or has ended. |
| `workflowId` | body | `string` | no | This is the workflow ID that will be used for the campaign calls. Can only be updated if campaign is not in progress or has ended. |
| `squadId` | body | `string` | no | This is the squad ID that will be used for the campaign calls. Can only be updated if campaign is not in progress or has ended. |
| `phoneNumberId` | body | `string` | no | This is the phone number ID that will be used for the campaign calls. Can only be updated if campaign is not in progress or has ended. Note: `phoneNumberId` and `dialPlan` are mutually exclusive. |
| `dialPlan[]` | body | `array<object>` | no | This is a list of dial entries, each specifying a phone number and the customers to call using that number. Can only be updated if campaign is not in progress or has ended. Note: phoneNumberId and dialPlan are mutually exclusive. |
| `schedulePlan` | body | `object` | no | — |
| `status` | body | `string` | no | This is the status of the campaign. Can only be updated to 'ended' if you want to end the campaign. When set to 'ended', it will delete all scheduled calls. Calls in progress will be allowed to complete. |
