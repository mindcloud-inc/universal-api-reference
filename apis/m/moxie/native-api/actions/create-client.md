# Create Client with Moxie

Creates a new client in Moxie.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/clients/create`
- **Base URL:** `https://pod01.withmoxie.com/api/public`
- **Official documentation:** [Create Client](https://help.withmoxie.com/en/articles/8160175-create-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Business name for the client. |
| `clientType` | body | `string` | yes | Either Client or Prospect. |
| `currency` | body | `string` | yes | ISO 4217 currency code for the client. |
| `website` | body | `string` | no | Website URL for the client. |
| `phone` | body | `string` | no | Primary phone number for the client. |
| `notes` | body | `string` | no | Internal notes for the client. |
| `paymentTerms` | body | `object` | no | Payment terms object for the client. |
| `contacts` | body | `list<object>` | no | Optional list of contacts to create with the client. |
