# Get Visitor with Topia

Retrieves a visitor from a Topia world.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/world/:urlSlug/visitors/:visitorId`
- **Base URL:** `https://api.topia.io/api`
- **Official documentation:** [Get Visitor](https://api.topia.io/api-docs/paths/v1/visitor.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlSlug` | path | `string` | yes | Topia world URL slug. |
| `visitorId` | path | `string` | yes | Identifier for the visitor. |
