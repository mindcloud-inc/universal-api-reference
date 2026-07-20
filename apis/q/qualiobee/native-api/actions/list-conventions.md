# List Conventions with Qualiobee

Retrieves conventions from Qualiobee.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organizationUuid/convention`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [List Conventions](https://app.qualiobee.fr/api/doc/#/Convention/PublicConventionController_getMany)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | — |
| `withDeleted` | query | `boolean` | no | — |
| `relations` | query | `list<string>` | no | Send multiple values as a array. |
| `uuid` | query | `string` | no | — |
| `isDisabled` | query | `boolean` | no | — |
