# BulkSMS: Show Message

Retrieves a message from BulkSMS by ID.

```
GET https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/show-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/show-message?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/show-message?${params}`, {
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
| `id` | string | yes | The BulkSMS message ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "creditCost": 1,
      "encoding": "string",
      "from": "string",
      "id": "string",
      "numberOfParts": 1,
      "relatedSentMessageId": "string",
      "status": {},
      "submission": {},
      "to": "string",
      "type": "string",
      "userSuppliedId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `creditCost` | number |  |
| `encoding` | string |  |
| `from` | string |  |
| `id` | string |  |
| `numberOfParts` | number |  |
| `relatedSentMessageId` | string |  |
| `status` | object |  |
| `submission` | object |  |
| `to` | string |  |
| `type` | string |  |
| `userSuppliedId` | string |  |

## Native endpoint

Through the native BulkSMS API, this operation is `GET /messages/:id` (base URL `https://api.bulksms.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-message.md) for the provider-specific parameters and requirements.

