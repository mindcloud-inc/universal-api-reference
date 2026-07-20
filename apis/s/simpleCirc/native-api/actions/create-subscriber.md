# Create Subscriber with SimpleCirc

Creates a new subscriber in SimpleCirc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.2/subscribers`
- **Base URL:** `https://simplecirc.com`
- **Official documentation:** [Create Subscriber](https://simplecirc.com/docs/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `email` | body | `string` | no |
| `company` | body | `string` | no |
| `address_1` | body | `string` | no |
| `address_2` | body | `string` | no |
| `city` | body | `string` | no |
| `state` | body | `string` | no |
| `zipcode` | body | `string` | no |
| `country` | body | `string` | no |
| `custom_fields` | body | `object` | no |
