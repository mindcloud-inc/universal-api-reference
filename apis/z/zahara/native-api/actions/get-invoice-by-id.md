# Get Invoice By ID with Zahara

Retrieves an invoice by ID from Zahara.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/{businessUnitApiKey}/Invoice/Get/{{documentId}}`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [Get Invoice By ID](https://ask.zaharasoftware.com/api-docs/get-invoices-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `number` | yes | Invoice document ID. |
