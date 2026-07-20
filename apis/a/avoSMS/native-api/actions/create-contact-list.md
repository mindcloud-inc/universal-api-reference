# Create Contact List with AvoSMS

Creates a new contact list in AvoSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contact/list/create`
- **Base URL:** `https://api.avosms.com`
- **Official documentation:** [Create Contact List](https://www.avosms.com/en/api/documentation/contact/list/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listContactName` | body | `string` | yes | Name of the contact list |
| `listContactCountryCode` | body | `string` | yes | ISO2 country code of the contact list |
