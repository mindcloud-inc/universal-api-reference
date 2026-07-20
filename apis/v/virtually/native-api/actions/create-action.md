# Create Action with Virtually

Creates a new action in Virtually.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/orgs/:orgId/actions`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [Create Action](https://app.tryvirtually.com/api/docs#/Actions/ActionsController_create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `message` | body | `object` | yes |
| `message.subject` | body | `string` | yes |
| `message.content` | body | `string` | yes |
| `channel` | body | `object` | yes |
| `channel.type` | body | `string` | yes |
| `channel.id` | body | `string` | no |
| `channel.sendAs` | body | `string` | no |
