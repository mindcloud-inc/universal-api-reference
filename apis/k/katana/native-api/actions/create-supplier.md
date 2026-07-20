# Create Supplier with Katana

Creates a new supplier in Katana.

## Endpoint

- **Method:** `POST`
- **Path:** `/suppliers`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Create Supplier](https://developer.katanamrp.com/reference/create-supplier)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `currency` | body | `string` | no |
| `email` | body | `string` | no |
| `phone` | body | `string` | no |
| `comment` | body | `string` | no |
| `addresses[]` | body | `array<object>` | no |
| `addresses[].line_1` | body | `string` | no |
| `addresses[].line_2` | body | `string` | no |
| `addresses[].city` | body | `string` | no |
| `addresses[].state` | body | `string` | no |
| `addresses[].zip` | body | `string` | no |
| `addresses[].country` | body | `string` | no |
