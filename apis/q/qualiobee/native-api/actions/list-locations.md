# List Locations with Qualiobee

Retrieves locations from Qualiobee.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organizationUuid/location`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [List Locations](https://app.qualiobee.fr/api/doc/#/Location/PublicLocationController_getMany)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | — |
| `withDeleted` | query | `boolean` | no | — |
| `relations` | query | `list<string>` | no | Send multiple values as a array. |
| `uuid` | query | `string` | no | — |
| `addressLine1` | query | `string` | no | — |
| `addressLine2` | query | `string` | no | — |
| `postCode` | query | `string` | no | — |
| `city` | query | `string` | no | — |
| `country` | query | `string` | no | — |
