# SearchAPI - Google Search: Search Google

Finds Google web search results in SearchAPI.

```
GET https://connect.mindcloud.co/v1/universal/searchAPIGoogleSearch/latest/actions/search-google
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchAPI - Google Search `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchAPIGoogleSearch/latest/actions/search-google?connectionId=$CONNECTION_ID&q=companies%20providing%20developer%20documentation%20tools" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "companies providing developer documentation tools"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchAPIGoogleSearch/latest/actions/search-google?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | string | yes | Search terms to send to Google. Supports Google operators like site:, inurl:, intitle:, AND, and OR. Example: `companies providing developer documentation tools`. |
| `location` | string | no | Canonical Google location such as New York,United States. Use Find Supported Locations to discover valid values. Example: `New York,United States`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `device` | string | no | Google device profile for the search. Default: `desktop`. |
| `gl` | string | no | Google country code for localization. Defaults to us when omitted by SearchAPI. Default: `us`. Example: `us`. |
| `hl` | string | no | Google interface language code. Defaults to en when omitted by SearchAPI. Default: `en`. Example: `en`. |
| `page` | number | no | Search results page to return. SearchAPI defaults to page 1. Default: `1`. |
| `safe` | string | no | SafeSearch behavior. SearchAPI defaults to blur. Default: `blur`. |
| `timePeriod` | string | no | Restrict results to a supported relative time period such as last_day, last_week, or last_month. |
| `verbatim` | boolean | no | Force Google to use exact keywords and bypass automatic query modifications. |
| `kgmid` | string | no | Knowledge Graph entity identifier such as /m/02_286 or /g/11f555cn8l. |
| `uule` | string | no | Exact Google-encoded location. Do not use together with Location. |
| `lr` | string | no | Restrict results to document languages using Google lang_ values such as lang_en or lang_it\|lang_de. Example: `lang_en`. |
| `cr` | string | no | Restrict results to documents originating in a specific country using Google country restriction values. Example: `countryUS`. |
| `nfpr` | string | no | Set to 1 to exclude auto-corrected results. |
| `filter` | string | no | Set to 1 to enable duplicate-content and host-crowding filters, or 0 to disable them. |
| `timePeriodMin` | string | no | Start date for custom time filtering in MM/DD/YYYY format. Example: `01/01/2026`. |
| `timePeriodMax` | string | no | End date for custom time filtering in MM/DD/YYYY format. Example: `01/31/2026`. |
| `optimizationStrategy` | string | no | Controls request optimization: performance by default, or ads for higher ad collection success rate. Default: `performance`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": [
        {}
      ],
      "organic_results": [
        {}
      ],
      "pagination": {},
      "related_questions": [
        {}
      ],
      "search_information": {},
      "search_metadata": {},
      "search_parameters": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ads` | array<object> | Paid Google ad results when returned. |
| `organic_results` | array<object> | Organic Google web results. |
| `pagination` | object | Pagination links and next page details when available. |
| `related_questions` | array<object> | Related question results when returned. |
| `search_information` | object | Google search summary such as displayed query and total results. |
| `search_metadata` | object | SearchAPI metadata including status, timing, and result URLs. |
| `search_parameters` | object | Resolved Google search parameters used for the request. |

## Native endpoint

Through the native SearchAPI - Google Search API, this operation is `GET /search` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google.md) for the provider-specific parameters and requirements.

