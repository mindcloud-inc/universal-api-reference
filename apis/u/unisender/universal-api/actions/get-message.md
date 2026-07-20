# Unisender: Get Message

Retrieves a message from Unisender.

```
GET https://connect.mindcloud.co/v1/universal/unisender/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unisender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unisender/latest/actions/get-message?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unisender/latest/actions/get-message?${params}`, {
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
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native Unisender API, this operation is `GET /getMessage` (base URL `https://api.unisender.com/en/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

