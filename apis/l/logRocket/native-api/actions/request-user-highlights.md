# Request User Highlights with LogRocket

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:orgId/apps/:projectId/highlights/`
- **Base URL:** `https://api.logrocket.com/v1`
- **Official documentation:** [Request User Highlights](https://docs.logrocket.com/docs/session-highlights-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userEmail` | body | `string` | no | Email of a user identified in LogRocket. Either User Email or User ID is required by LogRocket. |
| `userID` | body | `string` | no | ID of a user identified in LogRocket. Either User Email or User ID is required by LogRocket. |
| `question` | body | `string` | no | Optional question for Galileo to answer about the selected sessions. |
| `timeRange` | body | `object` | no | Optional object with startMs and endMs epoch millisecond values. |
| `webhookURL` | body | `string` | no | Optional URL where LogRocket should POST highlights when ready. |
