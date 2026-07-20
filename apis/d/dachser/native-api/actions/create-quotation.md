# Create Quotation with Dachser

Creates a new quotation in Dachser.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/quotations`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Create Quotation](https://api-portal.dachser.com/bi.b2b.portal/api/library/quotation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logisticsType` | body | `string` | no | D for distribution or P for procurement. |
| `saveQuotation` | body | `boolean` | no | Whether to save the quotation in eLogistics. |
| `transportOrder` | body | `object` | yes | Transport data for the quotation price calculation. |
| `acceptLanguage` | query | `string` | no | Optional language sent as the Accept-Language header. |
