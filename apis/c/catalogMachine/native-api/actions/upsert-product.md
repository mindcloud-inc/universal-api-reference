# Upsert Product with Catalog Machine

Creates or updates a product in Catalog Machine.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/:code`
- **Base URL:** `https://www.catalogmachine.com/api/v1`
- **Official documentation:** [Upsert Product](https://help.catalogmachine.com/en/articles/3667421-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Unique product code to create/update. |
