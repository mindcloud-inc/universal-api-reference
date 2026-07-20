# DataForB2B: Text To Filters

Converts text into DataForB2B search filters.

```
GET https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/text-to-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForB2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/text-to-filters?connectionId=$CONNECTION_ID&query=software%20engineers%20in%20San%20Francisco&category=people" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "software engineers in San Francisco",
  "category": "people"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/text-to-filters?${params}`, {
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
| `query` | string | yes | Natural-language text to convert into structured filters. Default: `software engineers in San Francisco`. |
| `category` | string | yes | Target category for the generated filters, such as people or company. Default: `people`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "filters": {},
      "requested_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `filters` | object |  |
| `requested_count` | number |  |

## Native endpoint

Through the native DataForB2B API, this operation is `POST /search/llm/filters` (base URL `https://api.dataforb2b.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/text-to-filters.md) for the provider-specific parameters and requirements.

