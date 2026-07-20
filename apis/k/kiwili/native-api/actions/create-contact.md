# Create Contact with Kiwili

Creates a new contact in Kiwili.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Create Contact](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | no | The contact email address. |
| `EnterpriseId` | body | `number` | yes | The enterprise ID the contact belongs to. |
| `FirstName` | body | `string` | yes | The contact first name. |
| `LastName` | body | `string` | yes | The contact last name. |
