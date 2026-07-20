# Change Invoice Status with Envoice

Updates an invoice status in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `invoice/changestatus`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Change Invoice Status](https://github.com/EmitKnowledge/Envoice/blob/master/invoice.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `number` | yes | Invoice ID. |
| `Status` | body | `string` | yes | Target invoice status. |
