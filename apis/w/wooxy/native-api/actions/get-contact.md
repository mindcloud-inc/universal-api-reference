# Get Contact with Wooxy

Retrieves a contact from your Wooxy account.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/contact/get`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Get Contact](https://wooxy.com/api-documentation/contacts/get-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactListId` | body | `string` | yes | Wooxy contact list ID. |
| `email` | body | `string` | no | Contact email address. |
| `phoneNumber` | body | `string` | no | Contact phone number in E.164 format. |
| `userId` | body | `string` | no | Contact user ID. |
