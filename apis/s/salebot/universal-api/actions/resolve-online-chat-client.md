# Salebot: Resolve Online Chat Client



```
GET https://connect.mindcloud.co/v1/universal/salebot/latest/actions/resolve-online-chat-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/resolve-online-chat-client?connectionId=$CONNECTION_ID&recipient=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recipient": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salebot/latest/actions/resolve-online-chat-client?${params}`, {
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
| `recipient` | string | yes | Online chat recipient identifier from the website integration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | number |  |

## Native endpoint

Through the native Salebot API, this operation is `GET /online_chat_client_id` (base URL `https://chatter.salebot.pro/api/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resolve-online-chat-client.md) for the provider-specific parameters and requirements.

