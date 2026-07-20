# Communi App: Get Conversation



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-conversation?connectionId=$CONNECTION_ID&id=event-1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "event-1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-conversation?${params}`, {
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
| `id` | string | yes | Default: `event-1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aErrorMessage": [
        "string"
      ],
      "error": "string",
      "errorMessage": "string",
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aErrorMessage` | array<string> |  |
| `error` | string |  |
| `errorMessage` | string |  |
| `valid` | boolean |  |

## Native endpoint

Through the native Communi App API, this operation is `GET /rest/conversation/:id` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation.md) for the provider-specific parameters and requirements.

