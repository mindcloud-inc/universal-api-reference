# Create Campaign with Vapi

Creates a new campaign in Vapi.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [Create Campaign](https://docs.vapi.ai/api-reference/campaigns/campaign-controller-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | This is the name of the campaign. This is just for your own reference. |
| `assistantId` | body | `string` | no | This is the assistant ID that will be used for the campaign calls. Note: Only one of assistantId, workflowId, or squadId can be used. |
| `workflowId` | body | `string` | no | This is the workflow ID that will be used for the campaign calls. Note: Only one of assistantId, workflowId, or squadId can be used. |
| `squadId` | body | `string` | no | This is the squad ID that will be used for the campaign calls. Note: Only one of assistantId, workflowId, or squadId can be used. |
| `phoneNumberId` | body | `string` | no | This is the phone number ID that will be used for the campaign calls. Required if dialPlan is not provided. Note: phoneNumberId and dialPlan are mutually exclusive. |
| `dialPlan[]` | body | `array<object>` | no | This is a list of dial entries, each specifying a phone number and the customers to call using that number. Use this when you want different phone numbers to call different sets of customers. Note: phoneNumberId and dialPlan are mutually exclusive. |
| `schedulePlan` | body | `object` | no | — |
| `customers[]` | body | `array<object>` | no | These are the customers that will be called in the campaign. Required if dialPlan is not provided. |
