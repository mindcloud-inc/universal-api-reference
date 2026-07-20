# List Contact Lists for Contact with Superchat

Retrieves contact lists for a Superchat contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/{contact_id}/contact-lists`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [List Contact Lists for Contact](https://developers.superchat.com/reference/getcontactlistsfromcontact)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The unique identifier of the contact |
