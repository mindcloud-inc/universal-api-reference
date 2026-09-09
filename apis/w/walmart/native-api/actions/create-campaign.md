# Create Campaign with Walmart

This API allows you to create a new Campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/advertising/sem/campaigns`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Create Campaign](https://developer.walmart.com/us-marketplace/reference/createcampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemsOperations.operationType` | body | `list<string>` | no | Type of operation to perform on campaign Items.  Allowed Values: `ADD`, `REMOVE` |
| `metadata` | body | `object` | no | Metadata for the campaign. |
| `metadata.name` | body | `string` | no | Name of the campaign. Allowed characters: letters, digits, dashes, underscores, and spaces. Maximum 255 characters allowed. Maximum length: 255. |
| `itemsOperations` | body | `object` | no | List of Operations to perform on campaign items. |
| `itemsOperations.skus[]` | body | `array<string>` | no | — |
| `metadata.startDate` | body | `string` | no | Start date of the campaign in yyyy-MM-dd format. |
| `metadata.endDate` | body | `string` | no | End date of the campaign in yyyy-MM-dd format. |
| `metadata.dailyBudget` | body | `number` | no | Daily budget allocated for the campaign. Must be a positive value with up to 2 decimal places. Daily budget must be between $5.00 and $2,500.00. |
| `metadata.totalBudget` | body | `number` | no | (optional) Total budget allocated for the campaign. Must be a positive value with up to 2 decimal places. Total budget must be between $5.00 and $250,000.00. Total budget must be greater than or equal to daily budget. |
| `metadata.biddingStrategyType` | body | `list<string>` | no | Bidding strategy type for the campaign. Defaults to `TARGET_ROAS` if not specified. |
| `metadata.targetRoas` | body | `number` | no | Target ROAS for the campaign. Must be a positive value between 1.00 and 20.00, with up to 2 decimal places.  Defaults to `3.5` if not specified. |
