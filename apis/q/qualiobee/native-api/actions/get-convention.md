# Get Convention with Qualiobee

Retrieves a convention from Qualiobee.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organizationUuid/convention/:conventionUuid`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Get Convention](https://app.qualiobee.fr/api/doc/#/Convention/PublicConventionController_getOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | The Qualiobee organization UUID used in the request path |
| `conventionUuid` | path | `string` | yes | The uuid of the convention to fetch |
| `withDeleted` | query | `boolean` | no | Include deleted conventions in the response |
| `relations` | query | `list<string>` | no | Related entities to include in the convention response Send multiple values as a array. |
