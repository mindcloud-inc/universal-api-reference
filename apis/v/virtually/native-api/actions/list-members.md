# List Members with Virtually

Retrieves members from your Virtually workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orgs/:orgId/members`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [List Members](https://app.tryvirtually.com/api/docs#/Members/MembersController_findAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sinceLastAttendedEventTime` | query | `string` | yes | Unix timestamp filter sent as a numeric string. Runtime evidence shows the API rejects requests when this value is omitted. |
