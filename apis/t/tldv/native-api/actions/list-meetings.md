# List Meetings with tl:dv

Retrieves meetings from tl:dv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1alpha1/meetings`
- **Base URL:** `https://pasta.tldv.io`
- **Official documentation:** [List Meetings](https://doc.tldv.io/index.html#tag/Meetings/operation/GetMeetings.GetMeetingById)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search meetings by keyword. |
| `from` | query | `date` | no | Return meetings from this date forward. |
| `to` | query | `date` | no | Return meetings up to this date. |
| `onlyParticipated` | query | `boolean` | no | Only include meetings the authenticated user participated in. |
| `meetingType` | query | `string` | no | Filter meetings by type. |
