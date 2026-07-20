# Update Contact with Alegra

Updates an existing contact in Alegra.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://api.alegra.com/api/v1`
- **Official documentation:** [Update Contact](https://developer.alegra.com/reference/editcontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `identificationObject.number` | body | `string` | no | Use for country-specific contact versions that require a structured identification object, such as Peru. |
| `identificationObject.type` | body | `string` | no | Use for country-specific contact versions that require a structured identification object, such as Peru. |
| `name` | body | `string` | yes | — |
| `identification` | body | `string` | no | — |
| `address.city` | body | `string` | no | — |
| `address.address` | body | `string` | no | — |
| `phonePrimary` | body | `string` | no | — |
| `phoneSecondary` | body | `string` | no | — |
| `mobile` | body | `string` | no | — |
| `seller` | body | `string` | no | — |
| `priceList` | body | `string` | no | — |
| `term` | body | `string` | no | — |
| `creditLimit` | body | `number` | no | — |
| `email` | body | `string` | no | — |
| `type` | body | `string` | no | — |
| `status` | body | `string` | no | — |
| `fax` | body | `string` | no | — |
| `accounting.debtToPay` | body | `string` | no | — |
| `accounting.accountReceivable` | body | `string` | no | — |
| `internalContacts[].name` | body | `string` | no | — |
| `internalContacts[].lastName` | body | `string` | no | — |
| `internalContacts[].email` | body | `string` | no | — |
| `internalContacts[].mobile` | body | `string` | no | — |
| `internalContacts[].phone` | body | `string` | no | — |
| `internalContacts[].sendNotifications` | body | `string` | no | — |
| `ignoreRepeated` | body | `boolean` | no | — |
| `statementAttached` | body | `string` | no | — |
