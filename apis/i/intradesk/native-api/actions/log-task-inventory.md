# Log Task Inventory with Intradesk

Logs task inventory usage in Intradesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/changes/v1/TaskInventory`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [Log Task Inventory](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/TaskInventory/put_v1_TaskInventory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | TaskInventoryRequestModel JSON object request body documented by Intradesk Changes API. |
