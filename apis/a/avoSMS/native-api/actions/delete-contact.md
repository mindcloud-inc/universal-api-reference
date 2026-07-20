# Delete Contact with AvoSMS

Deletes an existing contact from AvoSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contact/delete`
- **Base URL:** `https://api.avosms.com`
- **Official documentation:** [Delete Contact](https://www.avosms.com/en/api/documentation/contact/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listContactId` | body | `string` | yes | Contact list ID |
| `contactTelephoneNumber` | body | `string` | yes | Phone number of the contact to delete |
