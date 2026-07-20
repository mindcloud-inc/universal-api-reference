# Search Contacts with serviceminder.io

Finds contacts in ServiceMinder by name, email, phone, or address.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/locate`
- **Base URL:** `https://serviceminder.com/api`
- **Official documentation:** [Search Contacts](https://serviceminder.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AddressSearch` | body | `string` | no | Search contacts by address. |
| `EmailSearch` | body | `string` | no | Search contacts by email. |
| `NameSearch` | body | `string` | no | Search contacts by name. |
| `PhoneSearch` | body | `string` | no | Search contacts by phone. |
| `IdSearch` | body | `number` | no | Search contacts by identifier. |
