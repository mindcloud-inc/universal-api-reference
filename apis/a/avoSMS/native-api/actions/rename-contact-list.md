# Rename Contact List with AvoSMS

Updates an existing contact list in AvoSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contact/list/rename`
- **Base URL:** `https://api.avosms.com`
- **Official documentation:** [Rename Contact List](https://www.avosms.com/en/api/documentation/contact/list/rename)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listContactId` | body | `string` | yes | Contact list ID |
| `listContactName` | body | `string` | yes | New contact list name |
