# Create Campaign Order with Giftbit

Creates a Giftbit campaign order for emailed or shortlink rewards.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign`
- **Base URL:** `https://api-testbed.giftbit.com/papi/v1`
- **Official documentation:** [Create Campaign Order](https://www.giftbit.com/api-documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `string` | yes |
| `gift_template` | body | `string` | no |
| `message` | body | `string` | no |
| `subject` | body | `string` | no |
| `contacts[].email` | body | `string` | no |
| `contacts[].firstname` | body | `string` | no |
| `contacts[].lastname` | body | `string` | no |
| `price_in_cents` | body | `number` | yes |
| `brand_codes[]` | body | `array<string>` | no |
| `region` | body | `string` | no |
| `expiry` | body | `date` | no |
| `delivery_type` | body | `string` | no |
| `link_count` | body | `number` | no |
