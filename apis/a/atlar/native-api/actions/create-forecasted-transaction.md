# Create forecasted transaction with Atlar

Creates a forecasted transaction in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/analytics/v2beta/forecasted-transactions`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Create forecasted transaction](https://docs.atlar.com/reference/post-analytics-v2beta-forecasted-transactions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `parent` | body | `string<string>` | yes |
| `description` | body | `string<string>` | yes |
| `amount` | body | `string<string>` | yes |
| `date` | body | `date<string>` | yes |
| `origin` | body | `object<string>` | yes |
