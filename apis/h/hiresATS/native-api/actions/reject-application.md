# Reject Application with 100Hires ATS

Rejects an application in 100Hires ATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/:id/reject`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Reject Application](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Application ID to reject. |
| `rejection_reason_id` | body | `number` | no | Optional rejection reason ID. |
| `suppress_notification` | body | `boolean` | no | Whether to suppress the rejection notification. |
| `include` | query | `string` | no | Comma-separated related application resources to include. |
