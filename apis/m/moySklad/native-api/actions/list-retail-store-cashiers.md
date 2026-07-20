# List cashier retail store cashiers with MoySklad

Retrieves cashier retail store cashiers from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `entity/retailstore/:retailStoreId/cashiers`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [List cashier retail store cashiers](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-kassir)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `retailStoreId` | path | `string` | yes | MoySklad retail store ID. |
