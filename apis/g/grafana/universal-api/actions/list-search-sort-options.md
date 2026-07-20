# Grafana: List Search Sort Options

Retrieves search sort options from Grafana.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/list-search-sort-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/list-search-sort-options?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/list-search-sort-options?${params}`, {
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
      "sortOptions": [
        {
          "description": "string",
          "displayName": "Ava Chen",
          "meta": "string",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sortOptions[].description` | string |  |
| `sortOptions[].displayName` | string |  |
| `sortOptions[].meta` | string |  |
| `sortOptions[].name` | string |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /search/sorting` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-search-sort-options.md) for the provider-specific parameters and requirements.

