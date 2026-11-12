# Writeback Invoice as Exported with ServiceTitan

## Endpoint

- **Method:** `POST`
- **Path:** `accounting/v2/tenant/{tenant}/invoices/markasexported`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Writeback Invoice as Exported](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/Invoices_MarkAsExported)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Root request array. Add one object per invoice to mark as exported. Send multiple values as a array. |
| `invoiceId` | body | `number` | yes | ServiceTitan invoice ID. Required for every array item. |
| `externalId` | body | `string` | yes | External ERP reference, for example Mth=2026-11-01 00:00:00\|ARTrans=534. |
| `externalMessage` | body | `string` | no | Optional export result message stored with the ServiceTitan invoice. |
