# ManyChat: List Growth Tools

Retrieves growth tools from ManyChat.

```
GET https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/list-growth-tools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/list-growth-tools?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/list-growth-tools?${params}`, {
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
      "data": [
        {
          "id": 1,
          "name": "Ava Chen",
          "type": "string"
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].id` | number |  |
| `data[].name` | string |  |
| `data[].type` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ManyChat API, this operation is `GET /fb/page/getGrowthTools` (base URL `https://api.manychat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-growth-tools.md) for the provider-specific parameters and requirements.

