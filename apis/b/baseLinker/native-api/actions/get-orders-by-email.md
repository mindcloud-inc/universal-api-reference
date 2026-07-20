# Get Orders by Email with BaseLinker

Finds orders in BaseLinker by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Get Orders by Email](https://api.baselinker.com/index.php?method=getOrdersByEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address to search for in orders. |
