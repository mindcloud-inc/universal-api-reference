# DiceBear: List Avatar Styles



```
GET https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/list-avatar-styles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DiceBear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/list-avatar-styles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/list-avatar-styles?${params}`, {
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
      "styles": [
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
| `styles` | array<string> | Style names currently available in DiceBear 10.x. |

## Native endpoint

Through the native DiceBear API, this operation is `GET /` (base URL `https://api.dicebear.com/10.x`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-avatar-styles.md) for the provider-specific parameters and requirements.

