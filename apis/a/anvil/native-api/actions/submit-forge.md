# Submit Forge with Anvil

Submits data to a Forge webform in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Submit Forge](https://www.useanvil.com/docs/api/graphql/reference/#mutation-forgeSubmit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.forgeEid` | body | `string` | yes | Provide Forge EID for Submit Forge. |
| `variables.weldDataEid` | body | `string` | no | Provide Weld Data EID for Submit Forge. |
| `variables.submissionEid` | body | `string` | no | Provide Submission EID for Submit Forge. |
| `variables.payload` | body | `object` | yes | Provide Payload for Submit Forge. |
| `variables.enforcePayloadValidOnCreate` | body | `boolean` | no | Provide Enforce Payload Valid On Create for Submit Forge. |
| `variables.currentStep` | body | `number` | no | Provide Current Step for Submit Forge. |
| `variables.complete` | body | `boolean` | no | Provide Complete for Submit Forge. |
| `variables.isTest` | body | `boolean` | no | Provide Is Test for Submit Forge. |
| `variables.timezone` | body | `string` | no | Provide Timezone for Submit Forge. |
| `variables.webhookURL` | body | `string` | no | Provide Webhook URL for Submit Forge. |
| `variables.groupArrayId` | body | `string` | no | Provide Group Array ID for Submit Forge. |
| `variables.groupArrayIndex` | body | `number` | no | Provide Group Array Index for Submit Forge. |
