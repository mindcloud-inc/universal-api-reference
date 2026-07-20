# Create a lien for a business with Middesk

Creates a lien for a business in Middesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses/:business_id/liens`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Create a lien for a business](https://docs.middesk.com/reference/businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | ID of the business to create a lien for. |
| `debtors[]` | body | `array` | yes | Debtor entries for the lien filing. |
