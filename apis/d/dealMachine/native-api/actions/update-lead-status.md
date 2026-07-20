# Update Lead Status with DealMachine

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/leads/:lead_id/lead-status`
- **Base URL:** `https://api.dealmachine.com`
- **Official documentation:** [Update Lead Status](https://docs.dealmachine.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `number` | yes | The DealMachine lead ID. |
| `lead_status_id` | body | `number` | yes | The DealMachine lead status ID to assign. |
