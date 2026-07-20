# Generate Keyword Ideas with Google Ads

Generates keyword ideas in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId:generateKeywordIdeas`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Generate Keyword Ideas](https://developers.google.com/google-ads/api/reference/rpc/v22/KeywordPlanIdeaService/GenerateKeywordIdeas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID to generate keyword ideas for (without dashes). |
| `keywordSeed.keywords[]` | body | `array<string>` | yes | Keywords used as the idea-generation seed. |
| `language` | body | `string` | no | Resource name of the language constant. |
