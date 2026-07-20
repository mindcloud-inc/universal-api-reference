# List Customers with Synchroteam

Retrieves customers from Synchroteam, optionally filtered by change date.

## Endpoint

- **Method:** `GET`
- **Path:** `/Api/v2/Customer/List`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [List Customers](https://api.synchroteam.com/v2/#list-customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ChangedFrom` | query | `date` | no | Optional. Only return customers modified on or after this date (yyyy-mm-dd). |
