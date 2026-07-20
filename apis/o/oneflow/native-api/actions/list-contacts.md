# List Contacts with Oneflow

Retrieves contacts from Oneflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [List Contacts](https://developer.oneflow.com/reference/get-contacts-in-a-workspace)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes | The Oneflow workspace ID whose contacts should be listed. |
