# Get Shops with Eventix

Retrieves shops from Eventix.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/shop/:type`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get Shops](https://docs.weeztix.com/api/dashboard/get-shops)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `list<string>` | yes | How to handle archived Shops. Accepted values: `0`, `1`, `2`. |
