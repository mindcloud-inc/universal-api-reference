# List Contacts for Contact List with Superchat

Retrieves contacts for a Superchat contact list.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact-lists/{contact_list_id}/contacts`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [List Contacts for Contact List](https://developers.superchat.com/reference/listcontactsforcontactlist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_list_id` | path | `string` | yes | The unique identifier of the contact list |
| `before` | query | `string` | no | Specify the cursor before which objects should be returned. |
