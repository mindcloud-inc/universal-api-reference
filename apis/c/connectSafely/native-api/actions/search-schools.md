# Search schools with ConnectSafely

Search LinkedIn school IDs by name. Use it to find the `schoolId` that `POST /search/people` accepts in `filters.schoolIds`.

1. `POST /search/schools` with `{ "keywords": "Stanford" }` returns `{ "schoolId": "1792", "name": "Stanford University" }`.
2. `POST /search/people` with `{ "filters": { "schoolIds": ["1792"] } }`.

Results come from the same typeahead the LinkedIn people-search "Schools" filter uses, so the ids are exactly the ones the filter accepts. Returns up to 10 matches, in LinkedIn's own ranking order.

**Rate limit:** no per-account search quota is enforced on this lookup — only the general 30-calls-per-minute velocity limit. Resolve an id once and reuse it rather than looking it up on every request.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/schools`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Search schools](https://connectsafely.ai/docs/api/linkedin-search/post-search-schools-search-schools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use for the search. If not provided, uses the default account. |
| `keywords` | body | `string` | yes | School name to search for (e.g., "Stanford", "Pune", "MIT") |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `schools` | `array` |  |
| `schools[].name` | `string` | School display name |
| `schools[].schoolId` | `string` | Numeric id to pass as `filters.schoolIds` on people search |
| `count` | `number` | Number of schools returned |

### Example response

```json
{
  "success": true,
  "schools": [
    {
      "name": "Stanford University",
      "schoolId": "1792"
    },
    {
      "name": "Stanford Graduate School of Business",
      "schoolId": "2742"
    }
  ],
  "count": 2
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
