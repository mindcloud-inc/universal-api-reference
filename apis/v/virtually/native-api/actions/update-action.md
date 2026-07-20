# Update Action with Virtually

Updates an existing action in Virtually.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/orgs/:orgId/actions/:actionId`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [Update Action](https://app.tryvirtually.com/api/docs#/Actions/ActionsController_update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `actionId` | path | `string` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `message` | body | `object` | yes |
| `message.subject` | body | `string` | yes |
| `message.content` | body | `string` | yes |
| `channel` | body | `object` | yes |
| `channel.type` | body | `string` | yes |
| `channel.id` | body | `string` | no |
| `channel.sendAs` | body | `string` | no |
