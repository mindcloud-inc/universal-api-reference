# Void Document Group with Anvil

Voids a document group in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Void Document Group](https://www.useanvil.com/docs/api/graphql/reference/#mutation-voidDocumentGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.weldDataEid` | body | `string` | no | Provide Weld Data EID for Void Document Group. |
| `variables.eid` | body | `string` | no | Provide EID for Void Document Group. |
| `variables.voidedReason` | body | `string` | yes | Provide Voided Reason for Void Document Group. |
