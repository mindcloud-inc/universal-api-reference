# Send Review Session Invite with FTrack

Creates a review session invite in FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Send Review Session Invite](https://developer.ftrack.com/api/operations/send-review-session-invite-api-send-review-session-invite-sendreviewsessioninvite-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `review_session_invitee_id` | body | `string` | yes | Invitee record id to send the review session invitation to. |
