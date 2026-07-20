# List Transport Orders with Dachser

Retrieves transport orders from Dachser within a date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2/transportorders`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [List Transport Orders](https://api-portal.dachser.com/bi.b2b.portal/api/library/transportorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date-from` | query | `date` | no | Filter transport orders from this date. |
| `date-to` | query | `date` | no | Filter transport orders through this date. |
