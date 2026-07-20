# Get Session with Qualiobee

Retrieves a session from Qualiobee.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organizationUuid/session/:sessionUuid`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Get Session](https://app.qualiobee.fr/api/doc/#/Session/PublicSessionController_getOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | — |
| `sessionUuid` | path | `string` | yes | — |
| `withDeleted` | query | `boolean` | no | — |
| `relations` | query | `list<string>` | no | Send multiple values as a array. |
