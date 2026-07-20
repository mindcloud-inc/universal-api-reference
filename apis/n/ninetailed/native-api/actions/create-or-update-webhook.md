# Create Or Update Webhook with Ninetailed

## Endpoint

- **Method:** `PUT`
- **Path:** `/spaces/:spaceId/webhook_definitions/:webhookDefinitionId`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Create Or Update Webhook](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/webhooks/webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `webhookDefinitionId` | path | `string` | yes | ID to assign to the webhook definition or update. |
| `name` | body | `string` | yes | Webhook display name. |
| `url` | body | `string` | yes | Webhook target URL. |
| `topics[]` | body | `array<string>` | yes | Webhook topics such as Entry.publish. |
