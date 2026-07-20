# Assign Team Member To Lead with DealMachine

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/leads/:lead_id/assign-lead`
- **Base URL:** `https://api.dealmachine.com`
- **Official documentation:** [Assign Team Member To Lead](https://docs.dealmachine.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `number` | yes | The DealMachine lead ID. |
| `assign_to_id` | body | `number` | yes | The DealMachine team member ID to assign to the lead. |
