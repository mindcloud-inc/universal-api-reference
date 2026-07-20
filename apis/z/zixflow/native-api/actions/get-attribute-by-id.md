# Get Attribute By ID with Zixflow

Retrieves an attribute from Zixflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/attributes/:target/:targetId/:attributeId`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Get Attribute By ID](https://docs.zixflow.com/api-reference/attributes/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | path | `string` | yes | Target resource type for attributes. |
| `targetId` | path | `string` | yes | Target resource identifier for attributes. |
| `attributeId` | path | `string` | yes | Attribute identifier. |
