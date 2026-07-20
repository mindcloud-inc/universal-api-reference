# List Contacts with Lexware Office

Retrieves a list of contacts from Lexware Office.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [List Contacts](https://developers.lexware.io/docs/#contacts-endpoint-filtering-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter contacts by matching email address. |
| `name` | query | `string` | no | Filter contacts by matching contact name. |
| `number` | query | `number` | no | Filter contacts by customer or vendor number. |
| `customer` | query | `boolean` | no | Filter by whether the contact has the customer role. |
| `vendor` | query | `boolean` | no | Filter by whether the contact has the vendor role. |
