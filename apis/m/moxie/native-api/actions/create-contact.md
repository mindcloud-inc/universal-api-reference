# Create Contact with Moxie

Creates a new contact in Moxie.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/contacts/create`
- **Base URL:** `https://pod01.withmoxie.com/api/public`
- **Official documentation:** [Create Contact](https://help.withmoxie.com/en/articles/8160213-create-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first` | body | `string` | yes | Contact first name. |
| `last` | body | `string` | yes | Contact last name. |
| `email` | body | `string` | no | Contact email address. |
| `phone` | body | `string` | no | Contact phone number. |
| `clientName` | body | `string` | no | Existing client name to attach the contact to. |
| `defaultContact` | body | `boolean` | no | Whether this should be the default client contact. |
| `portalAccess` | body | `boolean` | no | Whether the contact should have portal access. |
| `invoiceContact` | body | `boolean` | no | Whether the contact should receive invoices. |
