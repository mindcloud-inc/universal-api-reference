# Create Tier with Ghost

Creates a new tier in Ghost.

## Endpoint

- **Method:** `POST`
- **Path:** `/tiers/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Create Tier](https://docs.ghost.org/admin-api/tiers/creating-a-tier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tiers[0].name` | body | `string` | yes | Name of the tier. |
| `tiers[0].description` | body | `string` | no | Public description for the tier. |
| `tiers[0].welcome_page_url` | body | `string` | no | Welcome page URL for the tier. |
| `tiers[0].visibility` | body | `string` | no | Tier visibility, such as public or none. |
| `tiers[0].monthly_price` | body | `number` | no | Monthly price in the smallest currency unit. |
| `tiers[0].yearly_price` | body | `number` | no | Yearly price in the smallest currency unit. |
| `tiers[0].currency` | body | `string` | no | Three-letter ISO currency code for paid tiers. |
| `tiers[0].benefits[]` | body | `array<string>` | no | List of public benefits for the tier. |
| `tiers[0].active` | body | `boolean` | no | Whether the tier should be active immediately. |
