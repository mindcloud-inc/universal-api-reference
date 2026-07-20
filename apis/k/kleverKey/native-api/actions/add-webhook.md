# Add Webhook with KleverKey

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/organizations/:organizationId/webhooks`
- **Base URL:** `https://api.kleverkey.com`
- **Official documentation:** [Add Webhook](https://portal.kleverkey.com/documentation/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `number` | yes |
| `name` | body | `string` | yes |
| `requestMethod` | body | `string` | yes |
| `requestUrl` | body | `string` | yes |
| `eventTypes[]` | body | `array<number>` | yes |
