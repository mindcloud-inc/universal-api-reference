# Update Ecommerce Category with DataCrush

Updates an ecommerce category in DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/ecommerce/v1/category/add`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Update Ecommerce Category](https://help.datacrush.la/hc/es-419/articles/35071971467405-API-Ecommerce-Categor%C3%ADas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categories_json` | body | `string` | yes | JSON array of category objects. Each object should include id, name, handle, url, description, and parent. |
