# Yay.com: List Time Diaries

Retrieves time diaries from Yay.com.

```
GET https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-time-diaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yay.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-time-diaries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-time-diaries?${params}`, {
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
      "elements": [
        {}
      ],
      "exceptions": [
        {}
      ],
      "name": "Ava Chen",
      "timezone": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `elements` | array<object> |  |
| `exceptions` | array<object> |  |
| `name` | string |  |
| `timezone` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Yay.com API, this operation is `GET /voip/out-of-hours` (base URL `https://api.yay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-diaries.md) for the provider-specific parameters and requirements.

