# Scrape do: Get Google trends data

Retrieves Google Trends data with Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-google-trends-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-google-trends-data?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-google-trends-data?${params}`, {
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
| `q` | string | yes | The Google Trends keyword. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "interest_by_region": [
        {}
      ],
      "interest_over_time": {},
      "related_queries": {},
      "related_topics": {},
      "search_parameters": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `interest_by_region` | array<object> | Regional trend breakdown. |
| `interest_over_time` | object | Interest-over-time timeseries data. |
| `related_queries` | object | Related query groups when requested. |
| `related_topics` | object | Related topic groups when requested. |
| `search_parameters` | object | Echo of Google Trends request parameters. |

## Native endpoint

Through the native Scrape do API, this operation is `GET /plugin/google/trends` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-trends-data.md) for the provider-specific parameters and requirements.

