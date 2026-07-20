# QStash: Bulk Cancel Messages

Cancels multiple messages in QStash by ID.

```
DELETE https://connect.mindcloud.co/v1/universal/qStash/latest/actions/bulk-cancel-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/bulk-cancel-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/bulk-cancel-messages?${params}`, {
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
| `messageIds[]` | array<string> | no | Specific message IDs to cancel. If provided, other filters are ignored. Accepts multiple values as an array. |
| `count` | number | no | Maximum number of messages to cancel. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `queueName` | string | no | Filter messages by queue name. |
| `url` | string | no | Filter messages by destination URL. |
| `label` | string | no | Filter messages by label. |

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

Through the native QStash API, this operation is `DELETE /v2/messages` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-cancel-messages.md) for the provider-specific parameters and requirements.

