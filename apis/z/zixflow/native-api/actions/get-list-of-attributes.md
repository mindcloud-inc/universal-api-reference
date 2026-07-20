# Get List of Attributes with Zixflow

Retrieves attributes from Zixflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/attributes/:target/:targetId`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Get List of Attributes](https://docs.zixflow.com/api-reference/attributes/get-list-of-attributes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | path | `string` | yes | Target resource type for attributes. |
| `targetId` | path | `string` | yes | Target resource identifier for attributes. |
