# QStash: Cancel Message

Cancels a queued or scheduled message in QStash.

```
DELETE https://connect.mindcloud.co/v1/universal/qStash/latest/actions/cancel-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/cancel-message?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/cancel-message?${params}`, {
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
| `messageId` | string | yes | Identifier of the message to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelled": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelled` | number |  |

## Native endpoint

Through the native QStash API, this operation is `DELETE /v2/messages/:messageId` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-message.md) for the provider-specific parameters and requirements.

