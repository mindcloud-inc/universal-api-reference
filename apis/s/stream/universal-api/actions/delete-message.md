# Stream: Delete Message

Deletes an existing message from Stream.

```
DELETE https://connect.mindcloud.co/v1/universal/stream/latest/actions/delete-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/stream/latest/actions/delete-message?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stream/latest/actions/delete-message?${params}`, {
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
| `id` | string | yes | Message ID. |
| `hard` | boolean | no | Whether to hard delete the message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": "string",
      "message": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | string |  |
| `message` | object |  |

## Native endpoint

Through the native Stream API, this operation is `DELETE /messages/:id` (base URL `https://chat.stream-io-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-message.md) for the provider-specific parameters and requirements.

