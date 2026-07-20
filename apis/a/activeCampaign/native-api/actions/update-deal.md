# Update Deal with ActiveCampaign

Updates an existing deal in ActiveCampaign.

## Endpoint

- **Method:** `PUT`
- **Path:** `/deals/:id`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [Update Deal](https://developers.activecampaign.com/reference/update-a-deal-new)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The deal ID. |
| `deal` | body | `object` | no | — |
| `deal.title` | body | `string` | no | — |
| `deal.description` | body | `string` | no | — |
| `deal.account` | body | `string` | no | — |
| `deal.contact` | body | `string` | no | — |
| `deal.value` | body | `number` | no | — |
| `deal.currency` | body | `string` | no | — |
| `deal.group` | body | `string` | no | — |
| `deal.stage` | body | `string` | no | — |
| `deal.owner` | body | `string` | no | — |
| `deal.percent` | body | `number` | no | — |
| `deal.status` | body | `number` | no | — |
| `deal.fields[]` | body | `array<object>` | no | — |
