# Create BOM with MRPeasy

Creates a new BOM in MRPeasy.

## Endpoint

- **Method:** `POST`
- **Path:** `/boms`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Create BOM](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | body | `number` | yes | MRPeasy product ID for the BOM. |
| `title` | body | `string` | yes | BOM title. |
| `components` | body | `array<object>` | yes | Array of BOM components, for example [{"article_id":1,"quantity":1,"ord":"1"}]. |
