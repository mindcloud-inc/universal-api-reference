# Create Formation with Qualiobee

Creates a new formation in Qualiobee.

## Endpoint

- **Method:** `POST`
- **Path:** `/:organizationUuid/formation`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Create Formation](https://app.qualiobee.fr/api/doc/#/Formation/PublicFormationController_createOne)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes |
| `title` | body | `string` | no |
| `externalId` | body | `string` | no |
| `description` | body | `string` | no |
| `pedagogiqueMethode` | body | `string` | no |
| `prerequisites` | body | `string` | no |
| `audience` | body | `string` | no |
| `evaluationMethode` | body | `string` | no |
| `actionMethode` | body | `string` | no |
| `usingBeehelp` | body | `boolean` | no |
| `usingSignature` | body | `boolean` | no |
| `usingSignatureMedia` | body | `boolean` | no |
| `subtractType` | body | `string` | no |
| `specialtyCode` | body | `string` | no |
| `certifType` | body | `string` | no |
| `certifLevel` | body | `string` | no |
| `pricing.strategy` | body | `string` | no |
| `pricing.precision` | body | `string` | no |
| `pricing.moneyValue` | body | `number` | no |
| `pricing.taxRate` | body | `number` | no |
