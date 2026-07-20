# Create Direct Link Order with Giftbit

Creates a direct link reward order in Giftbit.

## Endpoint

- **Method:** `POST`
- **Path:** `/direct_links`
- **Base URL:** `https://api-testbed.giftbit.com/papi/v1`
- **Official documentation:** [Create Direct Link Order](https://www.giftbit.com/api-documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `string` | yes |
| `price_in_cents` | body | `number` | yes |
| `brand_codes[]` | body | `array<string>` | no |
| `region` | body | `string` | no |
| `link_count` | body | `number` | no |
| `expiry` | body | `date` | no |
