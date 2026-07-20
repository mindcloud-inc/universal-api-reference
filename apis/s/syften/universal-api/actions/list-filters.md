# Syften: List Filters

Retrieves saved keyword filters from Syften.

```
GET https://connect.mindcloud.co/v1/universal/syften/latest/actions/list-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syften `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syften/latest/actions/list-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syften/latest/actions/list-filters?${params}`, {
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
      "items": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<string> |  |

## Native endpoint

Through the native Syften API, this operation is `POST /api/0.0/filters/get` (base URL `https://syften.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-filters.md) for the provider-specific parameters and requirements.

