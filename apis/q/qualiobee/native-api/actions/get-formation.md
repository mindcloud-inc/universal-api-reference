# Get Formation with Qualiobee

Retrieves a formation from Qualiobee.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organizationUuid/formation/:formationUuid`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Get Formation](https://app.qualiobee.fr/api/doc/#/Formation/PublicFormationController_getOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | — |
| `formationUuid` | path | `string` | yes | — |
| `withDeleted` | query | `boolean` | no | — |
| `relations` | query | `list<string>` | no | Send multiple values as a array. |
