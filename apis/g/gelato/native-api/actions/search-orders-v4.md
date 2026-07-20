# Search Orders v4 with Gelato

Finds orders in Gelato v4 by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/orders:search`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Search Orders v4](https://dashboard.gelato.com/docs/orders/v4/search/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | no |
| `orderReferenceId` | body | `string` | no |
| `orderReferenceIds[]` | body | `array<string>` | no |
| `orderTypes[]` | body | `array<string>` | no |
| `channels[]` | body | `array<string>` | no |
| `countries[]` | body | `array<string>` | no |
| `currencies[]` | body | `array<string>` | no |
| `financialStatuses[]` | body | `array<string>` | no |
| `fulfillmentStatuses[]` | body | `array<string>` | no |
| `search` | body | `string` | no |
| `startDate` | body | `string` | no |
| `endDate` | body | `string` | no |
| `storeIds[]` | body | `array<string>` | no |
