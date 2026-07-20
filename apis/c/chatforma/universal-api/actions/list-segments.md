# Chatforma: List Segments

Retrieves audience segment records from Chatforma.

```
GET https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/list-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatforma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/list-segments?connectionId=$CONNECTION_ID&botId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/list-segments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Chatforma API, this operation is `GET /bots/:botId/segments` (base URL `https://api.pro.chatforma.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segments.md) for the provider-specific parameters and requirements.

