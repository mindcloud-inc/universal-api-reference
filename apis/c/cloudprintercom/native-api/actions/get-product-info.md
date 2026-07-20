# Get Product Info with Cloudprinter.com

Retrieves product details from Cloudprinter.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/cloudcore/1.0/products/info`
- **Base URL:** `https://api.cloudprinter.com`
- **Official documentation:** [Get Product Info](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#product-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference` | body | `string` | yes | Product reference returned by List Products. |
