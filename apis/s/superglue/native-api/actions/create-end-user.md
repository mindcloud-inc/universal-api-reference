# Create End User with Superglue

## Endpoint

- **Method:** `POST`
- **Path:** `/end-users`
- **Base URL:** `https://api.superglue.ai/v1`
- **Official documentation:** [Create End User](https://docs.superglue.cloud/api-reference/end-users-enterprise/create-end-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | body | `string` | no | Your application's user ID. Auto-generated if omitted. |
| `email` | body | `string` | no | End user's email address. |
| `name` | body | `string` | no | End user's display name. |
| `allowedSystems[]` | body | `array<string>` | no | Array of system IDs, or ["*"] for all systems. Defaults to no access. |
