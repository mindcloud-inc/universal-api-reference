# Publish Contract with Oneflow

Publishes a contract in Oneflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/contracts/:id/publish`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [Publish Contract](https://developer.oneflow.com/reference/publish-a-contract-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Oneflow contract ID. |
| `subject` | body | `string` | yes | The invitation email subject sent when the contract is published. |
| `message` | body | `string` | yes | The invitation message sent when the contract is published. |
