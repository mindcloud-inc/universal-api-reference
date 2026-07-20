# Delete Webhook with ReleaseNotes

Deletes a webhook from ReleaseNotes.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:projectId/webhooks/:webhookId`
- **Base URL:** `https://api.releasenotes.io/api/v1`
- **Official documentation:** [Delete Webhook](https://releasenotes.elevio.help/en/articles/87801-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. |
| `webhookId` | path | `string` | yes | The webhook ID returned by the list or create webhook endpoints. |
