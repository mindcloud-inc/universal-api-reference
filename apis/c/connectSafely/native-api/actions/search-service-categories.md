# Search service categories with ConnectSafely

Search LinkedIn service-category ids by name, for `POST /search/people` `filters.serviceCategories`.

1. `POST /search/service-categories` with `{ "keywords": "Fina" }` returns `{ "serviceCategoryId": "826", "name": "Financial Analysis" }`.
2. `POST /search/people` with `{ "filters": { "serviceCategories": ["826"] } }`.

The ids are opaque and not guessable (Financial Analysis is `826`, Accounting is `71`), and LinkedIn answers an unrecognised id with 200 and zero results rather than an error — so without this lookup a wrong id is indistinguishable from "nobody matched". Returns up to 10 matches in LinkedIn's ranking order.

**Rate limit:** no per-account search quota is enforced on this lookup — only the general 30-calls-per-minute velocity limit. Resolve an id once and reuse it rather than looking it up on every request.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/service-categories`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Search service categories](https://connectsafely.ai/docs/api/linkedin-search/post-search-service-categories-search-service-categories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use for the search. If not provided, uses the default account. |
| `keywords` | body | `string` | yes | Service category name to search for (e.g., "Fina", "Marketing", "Accounting") |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `serviceCategories` | `array` |  |
| `serviceCategories[].name` | `string` | Service category display name |
| `serviceCategories[].serviceCategoryId` | `string` | Id to pass as `filters.serviceCategories` on people search |
| `count` | `number` | Number of categories returned |

### Example response

```json
{
  "success": true,
  "serviceCategories": [
    {
      "name": "Financial Analysis",
      "serviceCategoryId": "826"
    },
    {
      "name": "Financial Reporting",
      "serviceCategoryId": "219"
    }
  ],
  "count": 2
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
