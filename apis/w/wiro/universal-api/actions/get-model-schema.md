# Wiro: Get Model Schema

Retrieves model parameters and details from Wiro.

```
GET https://connect.mindcloud.co/v1/universal/wiro/latest/actions/get-model-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wiro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiro/latest/actions/get-model-schema?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiro/latest/actions/get-model-schema?${params}`, {
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
      "errors": [
        "string"
      ],
      "result": true,
      "tool": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `result` | boolean |  |
| `tool` | array<object> |  |

## Native endpoint

Through the native Wiro API, this operation is `POST /Tool/Detail` (base URL `https://api.wiro.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model-schema.md) for the provider-specific parameters and requirements.

