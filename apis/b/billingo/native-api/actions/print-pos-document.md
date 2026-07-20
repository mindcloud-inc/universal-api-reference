# Print POS Document with Billingo

Retrieves a printable POS document from Billingo.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:id/print/pos`
- **Base URL:** `https://api.billingo.hu/v3`
- **Official documentation:** [Print POS Document](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Billingo document ID from the path. |
| `size` | query | `string` | yes | POS print paper size required by Billingo. |
