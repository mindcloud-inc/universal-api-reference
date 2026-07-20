# Prerender.io: List Domains Company Config

Retrieves company domain config from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-domains-company-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-domains-company-config?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-domains-company-config?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "avgCacheMinutes": 1,
      "numberOfNotCrawledURLs": 1,
      "numCache_g1l7": 1,
      "numCache_g30": 1,
      "numCache_g7l30": 1,
      "numCacheToday": 1,
      "pagesCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avgCacheMinutes` | number |  |
| `numberOfNotCrawledURLs` | number |  |
| `numCache_g1l7` | number |  |
| `numCache_g30` | number |  |
| `numCache_g7l30` | number |  |
| `numCacheToday` | number |  |
| `pagesCount` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/domains/company/config` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-domains-company-config.md) for the provider-specific parameters and requirements.

