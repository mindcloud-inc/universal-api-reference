# Create Weld Data with Anvil

Creates new weld data in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Create Weld Data](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createWeldData)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.weldEid` | body | `string` | yes | Provide Weld EID for Create Weld Data. |
| `variables.weldDataGroupEid` | body | `string` | no | Provide Weld Data Group EID for Create Weld Data. |
| `variables.isTest` | body | `boolean` | no | Provide Is Test for Create Weld Data. |
| `variables.webhookURL` | body | `string` | no | Provide Webhook URL for Create Weld Data. |
