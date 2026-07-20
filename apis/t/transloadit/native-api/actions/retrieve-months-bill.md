# Retrieve a month's bill with Transloadit

Retrieves a monthly bill from Transloadit.

## Endpoint

- **Method:** `GET`
- **Path:** `/bill/:billDate`
- **Base URL:** `https://api2.transloadit.com`
- **Official documentation:** [Retrieve a month's bill](https://transloadit.com/docs/api/bill-date-get/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billDate` | path | `string` | yes | The monthly bill to retrieve in YYYY-MM format. |
