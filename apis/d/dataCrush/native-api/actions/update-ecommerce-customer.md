# Update Ecommerce Customer with DataCrush

Updates an ecommerce customer in DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/ecommerce/v1/customer/add`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Update Ecommerce Customer](https://help.datacrush.la/hc/es-419/articles/35073317623693-API-Ecommerce-Clientes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customers_json` | body | `string` | yes | JSON array of customer objects. Each object must include id, email, first_name, and last_name. |
