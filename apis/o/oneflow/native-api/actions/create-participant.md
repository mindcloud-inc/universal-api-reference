# Create Participant with Oneflow

Creates a contract participant in Oneflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/contracts/:contractId/parties/:partyId/participants`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [Create Participant](https://developer.oneflow.com/reference/create-a-participant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractId` | path | `string` | yes | The Oneflow contract ID. |
| `partyId` | path | `string` | yes | The Oneflow contract party ID. |
| `name` | body | `string` | yes | The participant name. |
| `signatory` | body | `boolean` | no | Whether the participant is a signatory. |
| `delivery_channel` | body | `string` | no | How Oneflow should deliver the contract to the participant. |
| `email` | body | `string` | no | The participant email when required by the delivery channel. |
| `phone_number` | body | `string` | no | The participant phone number when required by the delivery channel. |
