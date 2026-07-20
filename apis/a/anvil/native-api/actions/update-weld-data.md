# Update Weld Data with Anvil

Updates existing weld data in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Update Weld Data](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateWeldData)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | yes | Provide EID for Update Weld Data. |
| `variables.isTest` | body | `boolean` | no | Provide Is Test for Update Weld Data. |
| `variables.isArchived` | body | `boolean` | no | Provide Is Archived for Update Weld Data. |
| `variables.isExpired` | body | `boolean` | no | Provide Is Expired for Update Weld Data. |
| `variables.pin` | body | `string` | no | Provide Pin for Update Weld Data. |
| `variables.webhookURL` | body | `string` | no | Provide Webhook URL for Update Weld Data. |
