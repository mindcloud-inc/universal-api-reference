# Create Deal with ActiveCampaign

Creates a new deal in ActiveCampaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/deals`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [Create Deal](https://developers.activecampaign.com/reference/create-a-deal-new)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `deal` | body | `object` | yes |
| `deal.title` | body | `string` | yes |
| `deal.description` | body | `string` | no |
| `deal.account` | body | `string` | yes |
| `deal.contact` | body | `string` | yes |
| `deal.value` | body | `number` | yes |
| `deal.currency` | body | `string` | yes |
| `deal.group` | body | `string` | yes |
| `deal.stage` | body | `string` | yes |
| `deal.owner` | body | `string` | yes |
| `deal.percent` | body | `number` | no |
| `deal.status` | body | `number` | no |
| `deal.fields[]` | body | `array<object>` | no |
