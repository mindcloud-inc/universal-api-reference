# Create Session with Qualiobee

Creates a new session in Qualiobee.

## Endpoint

- **Method:** `POST`
- **Path:** `/:organizationUuid/session`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Create Session](https://app.qualiobee.fr/api/doc/#/Session/PublicSessionController_createOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | — |
| `formationUuid` | body | `string` | yes | — |
| `externalId` | body | `string` | no | — |
| `learnerUuids` | body | `list<string>` | yes | Send multiple values as a array. |
| `name` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `usingBeehelp` | body | `boolean` | no | — |
| `usingSignature` | body | `boolean` | no | — |
| `usingSignatureMedia` | body | `boolean` | no | — |
| `subtractType` | body | `string` | no | — |
| `specialtyCode` | body | `string` | no | — |
| `certifType` | body | `string` | no | — |
| `certifLevel` | body | `string` | no | — |
| `isConventionDisabled` | body | `boolean` | no | — |
| `isConvocationDisabled` | body | `boolean` | no | — |
| `isAttestationDisabled` | body | `boolean` | no | — |
| `pricing.strategy` | body | `string` | no | — |
| `pricing.precision` | body | `string` | no | — |
| `pricing.moneyValue` | body | `number` | no | — |
| `pricing.taxRate` | body | `number` | no | — |
