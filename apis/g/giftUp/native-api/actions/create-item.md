# Create Item with Gift Up

## Endpoint

- **Method:** `POST`
- **Path:** `/items`
- **Base URL:** `https://api.giftup.app`
- **Official documentation:** [Create Item](https://developer.giftup.com/api#create-a-new-item)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
| `backingType` | body | `string` | no |
| `priceType` | body | `string` | no |
| `price` | body | `number` | yes |
| `value` | body | `number` | yes |
| `groupId` | body | `string` | no |
| `detailsURL` | body | `string` | no |
| `stockLevel` | body | `number` | no |
| `perOrderLimit` | body | `number` | no |
| `additionalTerms` | body | `string` | no |
| `sku` | body | `string` | no |
| `codes[]` | body | `array<string>` | no |
| `codes[]` | body | `array<string>` | no |
| `codes[]` | body | `array<string>` | no |
