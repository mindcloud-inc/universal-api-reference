# Create Impact Calculator with Pledge

Creates an impact calculator in Pledge.

## Endpoint

- **Method:** `POST`
- **Path:** `/impact_calculators`
- **Base URL:** `https://api.pledge.to/v1`
- **Official documentation:** [Create Impact Calculator](https://developer.pledge.to/api/#tag/Impact%20Calculators/operation/createImpactCalculator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Impact calculator name. |
| `icon` | body | `string` | yes | Impact calculator icon. |
| `color` | body | `string` | yes | Primary hex color. |
| `formula` | body | `string` | yes | Formula used to compute tracked amount or impact. |
| `description` | body | `string` | yes | Text displayed after the amount. |
| `organization_ids[]` | body | `array<string>` | no | Organizations to scope the calculator to. |
| `external_id` | body | `string` | no | Fundraiser ID to scope the calculator to. |
| `currency_symbol` | body | `string` | no | Currency symbol to display. |
| `info` | body | `string` | no | Additional information shown on the back of the calculator. |
