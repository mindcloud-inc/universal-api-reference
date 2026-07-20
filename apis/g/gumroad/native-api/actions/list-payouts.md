# List Payouts with Gumroad

Retrieves payouts from Gumroad.

## Endpoint

- **Method:** `GET`
- **Path:** `/payouts`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [List Payouts](https://gumroad.com/api#get-/payouts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `date` | no | Only return payouts after this date (YYYY-MM-DD). |
| `before` | query | `date` | no | Only return payouts before this date (YYYY-MM-DD). |
| `include_upcoming` | query | `boolean` | no | Set to false to exclude upcoming payouts. |
