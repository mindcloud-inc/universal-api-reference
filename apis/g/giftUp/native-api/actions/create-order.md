# Create Order with Gift Up

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://api.giftup.app`
- **Official documentation:** [Create Order](https://developer.giftup.com/api#create-an-order)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `purchaserName` | body | `string` | yes |
| `purchaserEmail` | body | `string` | no |
| `disableAllEmails` | body | `boolean` | no |
| `orderDate` | body | `date` | no |
| `referrer` | body | `string` | no |
| `revenue` | body | `number` | no |
| `tip` | body | `number` | no |
| `serviceFee` | body | `number` | no |
| `discount` | body | `number` | no |
| `itemDetails[]` | body | `array<object>` | yes |
| `recipientDetails` | body | `object` | no |
| `customFields[]` | body | `array<object>` | no |
| `salesTaxes[]` | body | `array<object>` | no |
| `metadata` | body | `object` | no |
