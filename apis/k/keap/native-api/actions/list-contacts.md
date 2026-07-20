# List Contacts with Keap

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [List Contacts](https://developer.keap.com/docs/restv2/#tag/Contact/operation/listContacts)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-delimited list of Contact properties to include in the response (e.g. given_name,family_name,email_addresses,company,phone_numbers). |
