# Tellephant: List incoming logs

Retrieves incoming message logs from Tellephant.

```
GET https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/list-incoming-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tellephant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/list-incoming-logs?connectionId=$CONNECTION_ID&startDate=24-04-2026&endDate=24-04-2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "24-04-2026",
  "endDate": "24-04-2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/list-incoming-logs?${params}`, {
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
| `startDate` | string | yes | Start date in DD-MM-YYYY format. Default: `24-04-2026`. Example: `24-04-2026`. |
| `endDate` | string | yes | End date in DD-MM-YYYY format. Default: `24-04-2026`. Example: `24-04-2026`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Optional page number for paginated log results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "contact_id": "string",
      "content_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "media_url": "https://example.com",
      "message_type": "string",
      "sender_name": "Ava Chen",
      "text": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `contact_id` | string |  |
| `content_type` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `media_url` | string |  |
| `message_type` | string |  |
| `sender_name` | string |  |
| `text` | string |  |
| `timestamp` | number |  |

## Native endpoint

Through the native Tellephant API, this operation is `POST /v1/user/logs` (base URL `https://api.tellephant.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-incoming-logs.md) for the provider-specific parameters and requirements.

