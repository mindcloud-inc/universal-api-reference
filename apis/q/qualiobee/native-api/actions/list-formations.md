# List Formations with Qualiobee

Retrieves formations from Qualiobee.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organizationUuid/formation`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [List Formations](https://app.qualiobee.fr/api/doc/#/Formation/PublicFormationController_getMany)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | — |
| `withDeleted` | query | `boolean` | no | — |
| `relations` | query | `list<string>` | no | Send multiple values as a array. |
| `uuid` | query | `string` | no | — |
| `externalId` | query | `string` | no | — |
| `title` | query | `string` | no | — |
| `description` | query | `string` | no | — |
| `state` | query | `string` | no | — |
| `usingSignature` | query | `boolean` | no | — |
| `usingSignatureMedia` | query | `boolean` | no | — |
| `usingBeehelp` | query | `boolean` | no | — |
| `pedagogiqueMethode` | query | `string` | no | — |
| `prerequisites` | query | `string` | no | — |
| `audience` | query | `string` | no | — |
| `evaluationMethode` | query | `string` | no | — |
| `actionMethode` | query | `string` | no | — |
| `subtractType` | query | `string` | no | — |
| `specialtyCode` | query | `string` | no | — |
| `certifType` | query | `string` | no | — |
| `certifLevel` | query | `string` | no | — |
