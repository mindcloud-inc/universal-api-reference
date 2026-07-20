# List Webinar Registrations with Zoho Meeting

Retrieves webinar registrations from Zoho Meeting.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:organizationId/registration/:webinarKey`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [List Webinar Registrations](https://www.zoho.com/meeting/api-integration/webinar-api/registration.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
| `webinarKey` | path | `string` | yes | Webinar key returned by Create Webinar or List Webinars. |
| `status` | query | `string` | yes | Registration approval status filter: 1 auto approval, 0 manual approval, 2 denied by organiser, 3 cancelled by registrant. |
| `sysId` | query | `string` | no | Optional event ID. |
