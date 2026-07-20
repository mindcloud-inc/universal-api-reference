# ITM Platform: Search Tasks



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-tasks?${params}`, {
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
      "list": [
        {}
      ],
      "page": 1,
      "pagerid": "string",
      "pageSize": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `list` | array<object> |  |
| `page` | number |  |
| `pagerid` | string |  |
| `pageSize` | number |  |
| `total` | number |  |

## Native endpoint

Through the native ITM Platform API, this operation is `POST /v2/tasks/search` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tasks.md) for the provider-specific parameters and requirements.

