# Get Contracts with Veryfi

Retrieves contracts from Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/contracts`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Get Contracts](https://docs.veryfi.com/api/contracts/get-contracts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Default value: 1 The page number. The response is capped to maximum of 50 results per page. |
| `page_size` | query | `number` | no | Default value: 50 The number of Documents per page. |
