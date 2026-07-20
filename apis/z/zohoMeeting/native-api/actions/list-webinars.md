# List Webinars with Zoho Meeting

Retrieves webinars from Zoho Meeting.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:organizationId/webinar.json`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [List Webinars](https://www.zoho.com/meeting/api-integration/webinar-api/list-of-webinar-api.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
| `listtype` | query | `string` | yes | Webinar list type: all, past, today, or upcoming. |
