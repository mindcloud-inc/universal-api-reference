# Upsert Customer with Recommand

Finds a customer in Recommand, or creates one if no match is found.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/customers`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Upsert Customer](https://recommand.eu/en/reference/customers/upsert-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | The street address of the customer |
| `city` | body | `string` | yes | The city of the customer |
| `country` | body | `string` | yes | The country code (ISO 3166-1 alpha-2) of the customer |
| `email` | body | `string` | no | The email address of the customer |
| `enterpriseNumber` | body | `string` | no | The enterprise number of the customer |
| `externalId` | body | `string` | no | The external ID of the customer. If provided without id, finds by externalId and updates or creates if not found. |
| `id` | body | `string` | no | The internal ID of the customer to update. If provided, updates by id. |
| `name` | body | `string` | yes | The name of the customer |
| `peppolAddresses[]` | body | `array<string>` | no | The Peppol addresses of the customer |
| `phone` | body | `string` | no | The phone number of the customer |
| `postalCode` | body | `string` | yes | The postal code of the customer |
| `vatNumber` | body | `string` | no | The VAT number of the customer |
