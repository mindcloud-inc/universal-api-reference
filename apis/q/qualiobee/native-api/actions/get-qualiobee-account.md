# Get Qualiobee Account with Qualiobee

Retrieves a Qualiobee account by UUID.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organizationUuid/qualiobee/:qualiobeeUuid`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Get Qualiobee Account](https://app.qualiobee.fr/api/doc/#/Qualiobee/PublicQualiobeeController_getOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | — |
| `qualiobeeUuid` | path | `string` | yes | — |
| `withDeleted` | query | `boolean` | no | — |
| `relations` | query | `list<string>` | no | Send multiple values as a array. |
