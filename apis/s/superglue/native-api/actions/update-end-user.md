# Update End User with Superglue

## Endpoint

- **Method:** `PATCH`
- **Path:** `/end-users/:endUserId`
- **Base URL:** `https://api.superglue.ai/v1`
- **Official documentation:** [Update End User](https://docs.superglue.cloud/api-reference/end-users-enterprise/update-end-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endUserId` | path | `string` | yes | Internal Superglue end-user ID. |
| `externalId` | body | `string` | no | Your application's user ID. |
| `email` | body | `string` | no | End user's email address. |
| `name` | body | `string` | no | End user's display name. |
| `allowedSystems[]` | body | `array<string>` | no | Array of system IDs, or ["*"] for all systems. |
