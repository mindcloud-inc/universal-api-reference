# Get Document Payments with Billingo

Retrieves payment history for a document in Billingo.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:id/payments`
- **Base URL:** `https://api.billingo.hu/v3`
- **Official documentation:** [Get Document Payments](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Billingo document ID from the path. |
