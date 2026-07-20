# Get All Campaigns With Filters with Dotdigital

Retrieves campaigns from Dotdigital with optional filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/campaigns/filtered`
- **Base URL:** `https://r2-api.dotmailer.com`
- **Official documentation:** [Get All Campaigns With Filters](https://developer.dotdigital.com/reference/get-all-campaigns-with-filters)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `~type` | query | `list<string>` | no | Accepted values: `Standard`, `Triggered`. |
| `~tags` | query | `string` | no | Only campaigns that contain all supplied tags are returned. Send multiple values as a string separated by `,`. |
| `~sentDate` | query | `date` | no | Return campaigns sent on or after this UTC ISO-8601 date-time. |
| `~statuses` | query | `list<string>` | no | Allowed values: Unsent, Sent, Sending, Paused, Cancelled, RequiresWorkflowApproval. Accepted values: `Cancelled`, `Paused`, `RequiresWorkflowApproval`, `Sending`, `Sent`, `Unsent`. Send multiple values as a string separated by `,`. |
