# Adyntel Universal API Examples

These examples use the MindCloud API key and Adyntel connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Meta Ads by Keyword

Finds Meta ads in Adyntel by keyword.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/search-meta-ads-by-keyword?connectionId=$CONNECTION_ID&keyword=shopify" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "shopify"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/search-meta-ads-by-keyword?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "active_status": "string",
      "ad_type": "string",
      "continuation_token": "string",
      "country_code": "string",
      "is_result_complete": true,
      "media_types": "string",
      "number_of_ads": 1,
      "platform": "string",
      "query": "string",
      "results": [
        {}
      ],
      "search_type": "string",
      "start_max_date": "string",
      "start_min_date": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Meta Ads by Keyword action reference](actions/search-meta-ads-by-keyword.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/adyntelAPI/latest/actions/search-meta-ads-by-keyword).
