# Get Invoice with serviceminder.io

Retrieves an invoice from ServiceMinder by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/get`
- **Base URL:** `https://serviceminder.com/api`
- **Official documentation:** [Get Invoice](https://serviceminder.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceId` | body | `number` | yes | Invoice identifier. |
| `IncludeContact` | body | `boolean` | no | Whether to include contact details. |
