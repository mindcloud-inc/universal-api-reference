# Export Review Session Feedback with FTrack

Creates a review session feedback export in FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Export Review Session Feedback](https://developer.ftrack.com/api/operations/delayed-job-api-delayed-job-exportreviewsessionfeedbackdelayedjob-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `review_session_id` | body | `string` | yes | Review session whose feedback should be exported. |
| `language` | body | `string` | no | Optional export language. |
