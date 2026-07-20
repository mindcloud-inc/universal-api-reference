# Marketing Master IO: Opt In Chat Sequence Subscriber

Opts a subscriber into a chat sequence in Marketing Master IO.

```
PUT https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/opt-in-chat-sequence-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/opt-in-chat-sequence-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chat_sequence_id": "string",
  "subscriber_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/opt-in-chat-sequence-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chat_sequence_id": "string",
    "subscriber_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chat_sequence_id` | string | yes |  |
| `subscriber_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | boolean |  |

## Native endpoint

Through the native Marketing Master IO API, this operation is `POST /v1/messenger/chat_sequences/:chat_sequence_id/:subscriber_id` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/opt-in-chat-sequence-subscriber.md) for the provider-specific parameters and requirements.

