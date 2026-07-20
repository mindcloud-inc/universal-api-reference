# Invision Community: List Featured Content



```
GET https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/list-featured-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invision Community `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/list-featured-content?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/list-featured-content?${params}`, {
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
      "page": 1,
      "perPage": 1,
      "results": [
        {}
      ],
      "totalPages": 1,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number |  |
| `perPage` | number |  |
| `results` | array<object> |  |
| `totalPages` | number |  |
| `totalResults` | number |  |

## Native endpoint

Through the native Invision Community API, this operation is `GET /core/promotions` (base URL `{{credentials.communityBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-featured-content.md) for the provider-specific parameters and requirements.

