# List Payments with U-ON

Retrieves payment records from U-ON within a date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment/list/{date_from}/{date_to}/{page}.json`
- **Base URL:** `https://api.u-on.ru/{key}`
- **Official documentation:** [List Payments](https://api.u-on.travel/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_from` | path | `date` | yes | date_from path parameter |
| `date_to` | path | `date` | yes | date_to path parameter |
