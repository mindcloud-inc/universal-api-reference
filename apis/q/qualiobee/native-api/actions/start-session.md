# Start Session with Qualiobee

Starts an existing session in Qualiobee.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:organizationUuid/session/:sessionUuid/go`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Start Session](https://app.qualiobee.fr/api/doc/#/Session/PublicSessionController_go)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes |
| `sessionUuid` | path | `string` | yes |
