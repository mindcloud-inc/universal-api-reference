# List Invoices with Evoliz

Retrieves invoices from Evoliz.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/invoices`
- **Base URL:** `https://www.evoliz.io`
- **Official documentation:** [List Invoices](https://evoliz.io/documentation#tag/Invoice/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1invoices/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientid` | query | `number` | no | Optional filter for one client. |
