# Invite User with KleverKey

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/organizations/:organizationId/invitations/user-invitation`
- **Base URL:** `https://api.kleverkey.com`
- **Official documentation:** [Invite User](https://portal.kleverkey.com/documentation/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `number` | yes |
| `emailOrUserId` | body | `string` | yes |
