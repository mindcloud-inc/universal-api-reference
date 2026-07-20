# Social Intents: Get Chat By ID

Retrieves a chat from Social Intents by ID.

```
GET https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/get-chat-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Social Intents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/get-chat-by-id?connectionId=$CONNECTION_ID&chatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/get-chat-by-id?${params}`, {
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
| `chatId` | string | yes | The Social Intents chat ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiStatus": "string",
      "apiStatusCode": "string",
      "apiStatusMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiStatus` | string |  |
| `apiStatusCode` | string |  |
| `apiStatusMessage` | string |  |

## Native endpoint

Through the native Social Intents API, this operation is `GET /chats` (base URL `https://www.socialintents.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat-by-id.md) for the provider-specific parameters and requirements.

