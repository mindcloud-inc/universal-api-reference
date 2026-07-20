# BulkSMS: List Related Messages

Retrieves received messages related to a sent BulkSMS message.

```
GET https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/list-related-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/list-related-messages?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/list-related-messages?${params}`, {
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
| `id` | string | yes | The sent message ID whose related received replies should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "from": "string",
      "id": "string",
      "relatedSentMessageId": "string",
      "status": {},
      "to": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `from` | string |  |
| `id` | string |  |
| `relatedSentMessageId` | string |  |
| `status` | object |  |
| `to` | string |  |
| `type` | string |  |

## Native endpoint

Through the native BulkSMS API, this operation is `GET /messages/:id/relatedReceivedMessages` (base URL `https://api.bulksms.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-related-messages.md) for the provider-specific parameters and requirements.

