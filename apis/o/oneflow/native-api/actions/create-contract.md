# Create Contract with Oneflow

Creates a contract in Oneflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/contracts/create`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [Create Contract](https://developer.oneflow.com/reference/create-a-contract)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | The Oneflow workspace ID where the contract will be created. |
| `template_id` | body | `number` | yes | The Oneflow template ID to use when creating the contract. |
