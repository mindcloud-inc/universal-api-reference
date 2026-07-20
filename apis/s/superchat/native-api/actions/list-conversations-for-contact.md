# List Conversations for Contact with Superchat

Retrieves conversations for a Superchat contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/{contact_id}/conversations`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [List Conversations for Contact](https://developers.superchat.com/reference/getconversationforcontact)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The unique identifier of the contact |
