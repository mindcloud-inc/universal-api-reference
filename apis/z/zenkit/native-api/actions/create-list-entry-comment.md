# Create List Entry Comment with Zenkit

Creates a comment on a Zenkit item.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/me/lists/:listAllId/entries/:listEntryAllId/activities`
- **Base URL:** `https://zenkit.com/api/v1`
- **Official documentation:** [Create List Entry Comment](https://app.zenkit.com/docs/api/activity/post-api-v1-users-me-lists-listallid-entries-listentryallid-activities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listAllId` | path | `string` | yes | The list all id |
| `listEntryAllId` | path | `string` | yes | The list entry all id |
