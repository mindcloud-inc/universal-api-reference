# Create Party with Oneflow

Creates a contract party in Oneflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/contracts/:contractId/parties`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [Create Party](https://developer.oneflow.com/reference/create-a-party)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractId` | path | `string` | yes | The Oneflow contract ID. |
| `name` | body | `string` | yes | The name of the contract party. |
| `type` | body | `string` | yes | The party type, such as company. |
| `participants[].name` | body | `string` | yes | The participant name for the new party. |
| `participants[].signatory` | body | `boolean` | no | Whether the participant is a signatory. |
| `participants[].delivery_channel` | body | `string` | no | How Oneflow should deliver the contract to the participant. |
| `participants[].email` | body | `string` | no | The participant email when required by the delivery channel. |
| `participants[].phone_number` | body | `string` | no | The participant phone number when required by the delivery channel. |
