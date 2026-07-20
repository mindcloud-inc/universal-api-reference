# List User's Contacts with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/users/me/contacts`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [List User's Contacts](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getUserContacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Contact type: company or external. |
