# Get Visitor Data Object with Topia

Retrieves a visitor's data object from Topia.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/world/:urlSlug/visitors/:visitorId/get-data-object`
- **Base URL:** `https://api.topia.io/api`
- **Official documentation:** [Get Visitor Data Object](https://api.topia.io/api-docs/paths/v1/getVisitorDataObject.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlSlug` | path | `string` | yes | Topia world URL slug. |
| `visitorId` | path | `string` | yes | Identifier for the visitor. |
