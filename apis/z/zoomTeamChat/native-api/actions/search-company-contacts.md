# Search Company Contacts with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Search Company Contacts](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/searchCompanyContacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_key` | query | `string` | yes | First name, last name, or email address of the contact to search for. |
| `query_presence_status` | query | `boolean` | no | Whether to include the contact's presence status. |
| `contact_types` | query | `string` | no | Comma-separated contact type codes. |
| `user_status` | query | `string` | no | User status such as active or inactive. |
