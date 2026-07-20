# List Businesses with GatherUp

Retrieves a list of businesses from GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses/get`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [List Businesses](https://app.gatherup.com/api/doc/businesses/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeDeletedBusinesses` | body | `number` | no | Set to 0 if you want to hide deleted businesses, default value is 1. |
| `page` | body | `number` | no | Page number, if not specified then page = 1 |
| `limit` | body | `number` | no | Number of items per page, if not specified then limit = 100 |
