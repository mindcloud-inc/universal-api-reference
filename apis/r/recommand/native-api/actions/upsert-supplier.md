# Upsert Supplier with Recommand

Finds a supplier in Recommand, or creates one if no match is found.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/suppliers`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Upsert Supplier](https://recommand.eu/en/reference/suppliers/upsert-supplier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | body | `string` | no | The external ID of the supplier. If provided without id, finds by externalId and updates or creates if not found. |
| `id` | body | `string` | no | The internal ID of the supplier to update. If provided, updates by id. |
| `name` | body | `string` | yes | The name of the supplier |
| `peppolAddresses[]` | body | `array<string>` | no | The Peppol addresses of the supplier |
| `vatNumber` | body | `string` | no | The VAT number of the supplier |
