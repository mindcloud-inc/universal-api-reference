# Create Affiliate Commission with LeadDyno

Creates a new commission for an affiliate in LeadDyno.

## Endpoint

- **Method:** `POST`
- **Path:** `/affiliates/:id/commissions`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Create Affiliate Commission](https://app.theneo.io/leaddyno/leaddyno-rest-api/commissions/post-affiliates-id-commissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency` | body | `string` | no | The commission currency code. |
| `id` | path | `number` | yes | The affiliate ID. |
| `note` | body | `string` | no | A note or description for the manual commission. |
| `amount` | body | `number` | yes | The commission amount to be added. |
