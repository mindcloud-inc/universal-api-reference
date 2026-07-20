# Update Impact Calculator with Pledge

Updates an impact calculator in Pledge.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/impact_calculators/[:id]`
- **Base URL:** `https://api.pledge.to/v1`
- **Official documentation:** [Update Impact Calculator](https://developer.pledge.to/api/#tag/Impact%20Calculators/operation/updateImpactCalculator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Impact calculator ID. |
| `name` | body | `string` | no | Impact calculator name. |
| `icon` | body | `string` | no | Impact calculator icon. |
| `color` | body | `string` | no | Primary hex color. |
| `formula` | body | `string` | no | Formula used to compute tracked amount or impact. |
| `description` | body | `string` | no | Text displayed after the amount. |
| `organization_ids[]` | body | `array<string>` | no | Organizations to scope the calculator to. |
| `external_id` | body | `string` | no | Fundraiser ID to scope the calculator to. |
| `currency_symbol` | body | `string` | no | Currency symbol to display. |
| `info` | body | `string` | no | Additional information shown on the back of the calculator. |
