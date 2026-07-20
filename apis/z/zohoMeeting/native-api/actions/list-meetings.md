# List Meetings with Zoho Meeting

Retrieves meetings from Zoho Meeting.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:organizationId/sessions.json`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [List Meetings](https://www.zoho.com/meeting/api-integration/meeting-api/list-of-meeting-api.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
| `listtype` | query | `string` | yes | Meeting list type: all, past, today, or upcoming. |
