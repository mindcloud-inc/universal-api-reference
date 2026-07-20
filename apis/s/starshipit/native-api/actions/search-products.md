# Search Products with Starshipit

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Search Products](https://api-docs.starshipit.com/#ccf0f10f-e370-45c0-ba5c-13bfaac80ca6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_term` | query | `string` | yes | "" or "shoe" (Mandatory) |
| `page_number` | query | `string` | no | — |
| `page_size` | query | `string` | no | Min: 10 Max: 2000 |
| `skip_records` | query | `string` | no | — |
| `sort_column` | query | `string` | no | Barcode \| BinLocation \| Brand \| Colour \| Country \| CustomsDescription \| DangerousGoodsType \| Height \| HSCode \| Length \| Manufacturer \| Materials \| Model \| Price \| Purpose \| Size \| Sku \| Title \| Weight \| Width |
| `sort_direction` | query | `string` | no | Ascending \| Descending |
