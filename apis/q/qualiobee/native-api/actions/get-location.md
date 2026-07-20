# Get Location with Qualiobee

Retrieves a location from Qualiobee.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organizationUuid/location/:locationUuid`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Get Location](https://app.qualiobee.fr/api/doc/#/Location/PublicLocationController_getOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | — |
| `locationUuid` | path | `string` | yes | — |
| `withDeleted` | query | `boolean` | no | — |
| `relations` | query | `list<string>` | no | Send multiple values as a array. |
