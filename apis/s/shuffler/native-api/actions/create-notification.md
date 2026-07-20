# Create Notification with Shuffler

Creates a notification in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/notifications`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Create Notification](https://shuffler.io/docs/API#create-a-notification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | yes | Notification description. |
| `org_id` | body | `string` | yes | Organization identifier. |
| `reference_url` | body | `string` | no | Optional reference URL. |
| `title` | body | `string` | yes | Notification title. |
