# Mark Invoice as Exported with ServiceTitan

Update Invoice record.

## Endpoint

- **Method:** `POST`
- **Path:** `accounting/v2/tenant/{tenant}/invoices/markasexported`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Mark Invoice as Exported](https://developer.servicetitan.io/api-details/#api=tenant-accounting-v2&operation=Invoices_GetList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array` | yes | [   {     "invoiceId": 0,     "externalId": "string",     "externalMessage": "string"   } ] |
