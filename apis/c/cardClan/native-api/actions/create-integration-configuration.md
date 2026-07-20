# Create Integration Configuration with CardClan

Creates a CardClan integration configuration for a card workflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/integration/config`
- **Base URL:** `https://app.cardclan.io/api`
- **Official documentation:** [Create Integration Configuration](https://docs.cardclan.io/api-reference/integration/config/create-config)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | User ID for the integration owner. |
| `workspaceId` | body | `string` | yes | Workspace ID for the configuration. |
| `cardId` | body | `string` | yes | Card ID for the configuration. |
