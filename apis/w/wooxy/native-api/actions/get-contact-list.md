# Get Contact List with Wooxy

Retrieves a contact list from Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/contact-list/get`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Get Contact List](https://wooxy.com/api-documentation/contact-list/get-contact-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactListId` | body | `string` | no | Contact list ID in Wooxy. |
| `domain` | body | `string` | no | Verified sender domain in Wooxy. |
| `domainId` | body | `string` | no | Unique Wooxy domain ID. |
