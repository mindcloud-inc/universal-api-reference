# Search Talents with Kalent

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/search/talents`
- **Base URL:** `https://app.kalent.ai/api`
- **Official documentation:** [Search Talents](https://docs.kalent.ai/api-reference/search-talents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters[]` | body | `array<object>` | yes | Required array of Kalent search filter objects. Each object follows the provider request shape and can include filterType, value, isRequired, isExcluded, isExactMatch, radius, and history. |
| `relatedSearchTransactionIds[]` | body | `array<string>` | no | Optional array of previous searchTransactionId values used by Kalent to continue searches without duplicate profiles. |
