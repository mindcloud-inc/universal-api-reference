# Topia: List Expressions

Retrieves available expressions from the Topia catalog.

```
GET https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-expressions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Topia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-expressions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-expressions?${params}`, {
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
      "expressionImage": "string",
      "id": "string",
      "isLive": true,
      "isPlatformExpression": true,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expressionImage` | string |  |
| `id` | string |  |
| `isLive` | boolean |  |
| `isPlatformExpression` | boolean |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Topia API, this operation is `GET /v1/expressions` (base URL `https://api.topia.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-expressions.md) for the provider-specific parameters and requirements.

