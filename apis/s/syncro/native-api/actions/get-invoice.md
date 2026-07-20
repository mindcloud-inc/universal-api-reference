# Get Invoice with Syncro

Retrieves an invoice from Syncro by ID or number.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices/:id`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [Get Invoice](https://api-docs.syncromsp.com/#/Invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Invoice identifier. Syncro's path schema documents this as an integer ID. |
