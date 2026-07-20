# Create Link Intent with Fintoc

Creates a link intent in Fintoc.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/link_intents`
- **Base URL:** `https://api.fintoc.com`
- **Official documentation:** [Create Link Intent](https://docs.fintoc.com/reference/create-link-intent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product` | body | `string` | yes | Product to request in the link intent (for example: movements). |
| `holder_type` | body | `string` | yes | Holder type (for example: individual). |
| `country` | body | `string` | yes | ISO 3166-1 alpha-2 country code (for example: cl). |
