# Create product with MoySklad

Creates a product in MoySklad.

## Endpoint

- **Method:** `POST`
- **Path:** `entity/product`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Create product](https://dev.moysklad.ru/doc/api/remap/1.2/#suschnosti-towar-sozdat-towar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Product name. Required by MoySklad for product creation. |
