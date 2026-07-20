# Get contact tags with Tellephant

Retrieves tags for a Tellephant contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/user/contacts/:contactId/tags`
- **Base URL:** `https://api.tellephant.com`
- **Official documentation:** [Get contact tags](https://app.tellephant.com/api-documentation#fetch-contact-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Contact phone number/contact ID in the path. |
