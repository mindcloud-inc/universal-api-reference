# Get Inventory with SquareSpace

Retrieves inventory from Squarespace by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.0/commerce/inventory/:ids`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Get Inventory](https://developers.squarespace.com/commerce-apis/inventory#get-inventory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Inventory variant IDs (comma-separated). |
