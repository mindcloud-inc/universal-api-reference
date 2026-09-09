# Check Eligibility of Items with Walmart

Check whether an item from your catalog meets the required conditions for Search Engine Marketing ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/advertising/sem/items/eligibility`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Check Eligibility of Items](https://developer.walmart.com/us-marketplace/reference/getcampaigndetails)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters[]` | body | `array<object>` | no |
| `filters[].field` | body | `string` | no |
| `filters[].values[]` | body | `array<string>` | no |
