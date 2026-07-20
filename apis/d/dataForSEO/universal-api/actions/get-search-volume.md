# DataForSEO: Get Search Volume

Retrieves keyword search volume from DataForSEO.

```
GET https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-search-volume
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForSEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-search-volume?connectionId=$CONNECTION_ID&keywords%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keywords[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-search-volume?${params}`, {
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
| `keywords[]` | array<string> | yes | Keywords to get search volume for. |
| `location_name` | string | no | Full location name in hierarchical comma-separated format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language_code` | string | no | Two-letter ISO language code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "competition": "string",
      "competitionIndex": 1,
      "cpc": 1,
      "highTopOfPageBid": 1,
      "keyword": "string",
      "lowTopOfPageBid": 1,
      "monthlySearches": {},
      "searchVolume": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `competition` | string | Competition bucket returned by DataForSEO. |
| `competitionIndex` | number | Competition index returned by the provider. |
| `cpc` | number | Average cost-per-click estimate. |
| `highTopOfPageBid` | number | Upper bound of the top-of-page bid estimate. |
| `keyword` | string | Keyword submitted for Google Ads search volume lookup. |
| `lowTopOfPageBid` | number | Lower bound of the top-of-page bid estimate. |
| `monthlySearches` | object | Monthly search volume breakdown keyed by year-month. |
| `searchVolume` | number | Estimated monthly search volume. |

## Native endpoint

Through the native DataForSEO API, this operation is `POST /v3/keywords_data/google_ads/search_volume/live.ai` (base URL `https://api.dataforseo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search-volume.md) for the provider-specific parameters and requirements.

