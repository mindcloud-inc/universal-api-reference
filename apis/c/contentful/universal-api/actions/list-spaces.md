# Contentful: List spaces



```
GET https://connect.mindcloud.co/v1/universal/contentful/latest/actions/list-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contentful `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentful/latest/actions/list-spaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentful/latest/actions/list-spaces?${params}`, {
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
        {
          "name": "Ava Chen",
          "sys": {
            "id": "string",
            "type": "string"
          }
        }
      ],
      "limit": 1,
      "skip": 1,
      "sys": {
        "type": "string"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].name` | string |  |
| `items[].sys.id` | string |  |
| `items[].sys.type` | string |  |
| `limit` | number |  |
| `skip` | number |  |
| `sys.type` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Contentful API, this operation is `GET /spaces` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-spaces.md) for the provider-specific parameters and requirements.

