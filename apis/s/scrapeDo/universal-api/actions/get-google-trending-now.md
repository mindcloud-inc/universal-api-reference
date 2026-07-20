# Scrape do: Get Google trending now

Retrieves Google trending searches with Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-google-trending-now
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-google-trending-now?connectionId=$CONNECTION_ID&geo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "geo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-google-trending-now?${params}`, {
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
| `geo` | string | yes | Country code for Google Trending Now. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "search_parameters": {},
      "trends": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `search_parameters` | object | Echo of trending-now request parameters. |
| `trends` | array<object> | Real-time trending topic entries. |

## Native endpoint

Through the native Scrape do API, this operation is `GET /plugin/google/trending` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-trending-now.md) for the provider-specific parameters and requirements.

