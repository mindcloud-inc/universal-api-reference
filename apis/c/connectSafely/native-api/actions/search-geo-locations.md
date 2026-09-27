# Search geo locations with ConnectSafely

Search for LinkedIn geo location IDs by place name. Use this endpoint to find location IDs that can be used as filters in other search endpoints (jobs, companies, people). Returns matching cities, regions, and countries.

**Rate limit:** no per-account search quota is enforced on this lookup — only the general 30-calls-per-minute velocity limit. Resolve an id once and reuse it rather than looking it up on every request.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/geo`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Search geo locations](https://connectsafely.ai/docs/api/linkedin-search/post-search-geo-search-geo-locations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use for the search. If not provided, uses the default account. |
| `keywords` | body | `string` | yes | Location name to search for (e.g., "San Francisco", "United States", "London") |
| `countryCodes` | body | `array` | no | Limit results to specific countries using ISO country codes (e.g., ["US", "GB"]) |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `locations` | `array` |  |
| `locations[].name` | `string` | Location name (city, region, or country) |
| `locations[].geoId` | `string` | LinkedIn geo ID for use in search filters |
| `locations[].countryCode` | `string` | ISO country code (e.g., "US", "GB") |
| `count` | `number` | Number of locations returned |

### Example response

```json
{
  "success": true,
  "locations": [
    {
      "name": "San Francisco Bay Area",
      "geoId": "90000084",
      "countryCode": "US"
    },
    {
      "name": "San Francisco, California, United States",
      "geoId": "102277331",
      "countryCode": "US"
    }
  ],
  "count": 2
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
