# Update Contact with TxtSync

Updates an existing contact in TxtSync.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://api.txtsync.com`
- **Official documentation:** [Update Contact](https://docs.txtsync.com/#update-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Contact identifier. |
| `FirstName` | body | `string` | no | Updated first name. |
| `LastName` | body | `string` | no | Updated last name. |
| `CompanyName` | body | `string` | no | Updated company name. |
