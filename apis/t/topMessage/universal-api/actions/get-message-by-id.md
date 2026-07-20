# TopMessage: Get Message By ID

Retrieves a message by ID from TopMessage.

```
GET https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/get-message-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TopMessage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/get-message-by-id?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/get-message-by-id?${params}`, {
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
| `messageId` | string | yes | The unique identifier of the TopMessage message to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | The message returned by TopMessage for the requested message ID. |

## Native endpoint

Through the native TopMessage API, this operation is `GET /v1/messages/:Id` (base URL `https://api.topmessage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-by-id.md) for the provider-specific parameters and requirements.

