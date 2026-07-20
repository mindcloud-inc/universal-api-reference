# Update Suppression List Contact with Postalytics

Updates a contact on a Postalytics suppression list.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/lists/suppression/contacts/:listId/:contactId`
- **Base URL:** `https://api.postalytics.com`
- **Official documentation:** [Update Suppression List Contact](https://docs.postalytics.com/references/postalytics-rest-api/update-suppression-list-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Address` | body | `string` | no | Mailing street address. |
| `City` | body | `string` | no | Mailing city. |
| `Country` | body | `string` | no | Mailing country code. |
| `Email` | body | `string` | no | Suppressed contact email address. |
| `FirstName` | body | `string` | no | Suppressed contact first name. |
| `LastName` | body | `string` | no | Suppressed contact last name. |
| `listId` | path | `number` | yes | Suppression list ID. |
| `State` | body | `string` | no | Mailing state or province. |
| `Zip` | body | `string` | no | Mailing postal code. |
| `contactId` | path | `number` | yes | Suppression contact ID. |
