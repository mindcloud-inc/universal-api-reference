# Add Access Group with KleverKey

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/organizations/:organizationId/access-groups`
- **Base URL:** `https://api.kleverkey.com`
- **Official documentation:** [Add Access Group](https://portal.kleverkey.com/documentation/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | — |
| `name` | body | `string` | yes | — |
| `lockIds[]` | body | `array<number>` | yes | — |
| `userIds[]` | body | `array<number>` | yes | — |
| `permissionType` | body | `number` | yes | 1 = Always, 2 = TimeProfile |
