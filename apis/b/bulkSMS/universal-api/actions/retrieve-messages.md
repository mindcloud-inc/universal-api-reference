# BulkSMS: Retrieve Messages

Retrieves sent or received messages from BulkSMS.

```
GET https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/retrieve-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/retrieve-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/retrieve-messages?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | URL-encoded BulkSMS message filter clauses, such as type=SENT or status.type=DELIVERED. |
| `sortOrder` | list | no | Message sort order. BulkSMS supports ASC or DESC. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "encoding": "string",
      "from": "string",
      "id": "string",
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
| `encoding` | string |  |
| `from` | string |  |
| `id` | string |  |
| `relatedSentMessageId` | string |  |
| `status` | object |  |
| `submission` | object |  |
| `to` | string |  |
| `type` | string |  |
| `userSuppliedId` | string |  |

## Native endpoint

Through the native BulkSMS API, this operation is `GET /messages` (base URL `https://api.bulksms.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-messages.md) for the provider-specific parameters and requirements.

