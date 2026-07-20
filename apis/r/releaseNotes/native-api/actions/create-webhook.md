# Create Webhook with ReleaseNotes

Creates a new webhook in ReleaseNotes.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/webhooks`
- **Base URL:** `https://api.releasenotes.io/api/v1`
- **Official documentation:** [Create Webhook](https://releasenotes.elevio.help/en/articles/87801-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. |
| `event` | body | `string` | yes | The webhook event to subscribe to. ReleaseNotes currently documents release_published. |
| `url` | body | `string` | yes | The HTTPS destination URL for webhook deliveries. |
