# Vestaboard: Read Current Message

Retrieves the current message from Vestaboard.

```
GET https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/read-current-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vestaboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/read-current-message?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/read-current-message?${params}`, {
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
      "currentMessage": {
        "appeared": 1,
        "id": "string",
        "layout": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentMessage.appeared` | number | Unix timestamp in milliseconds when the message appeared. |
| `currentMessage.id` | string | Vestaboard message identifier. |
| `currentMessage.layout` | string | Serialized layout matrix for the current board state. |

## Native endpoint

Through the native Vestaboard API, this operation is `GET /` (base URL `https://cloud.vestaboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-current-message.md) for the provider-specific parameters and requirements.

