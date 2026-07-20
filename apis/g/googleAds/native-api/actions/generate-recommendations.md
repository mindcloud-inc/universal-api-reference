# Generate Recommendations with Google Ads

Generates recommendations for your Google Ads account.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/recommendations:generate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Generate Recommendations](https://developers.google.com/google-ads/api/reference/rpc/v22/RecommendationService/GenerateRecommendations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID to generate recommendations for (without dashes). |
| `recommendationTypes[]` | body | `array<string>` | no | Optional recommendation types to generate. |
| `advertisingChannelType` | body | `string` | no | Optional channel type filter for recommendation generation. |
