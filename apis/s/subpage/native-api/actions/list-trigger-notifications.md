# List Trigger Notifications with Subpage

## Endpoint

- **Method:** `GET`
- **Path:** `/call/api/zapier/listtrigger`
- **Base URL:** `https://editor.subpage.app`
- **Official documentation:** [List Trigger Notifications](https://helpcenter.subpage.app/article/zapier-api-integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | query | `string` | yes | Subpage event type to list notifications for, such as new_lead or new_article. |
