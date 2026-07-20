# Create Contact with TxtSync

Creates a new contact in TxtSync.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.txtsync.com`
- **Official documentation:** [Create Contact](https://docs.txtsync.com/#add-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MobileNumber` | body | `string` | yes | Contact mobile number in international format. |
| `FirstName` | body | `string` | no | Contact first name. |
| `LastName` | body | `string` | no | Contact last name. |
| `AllowSMS` | body | `boolean` | no | Whether the contact allows SMS. |
