# Channels: Create Recordings Archive Link

Creates a recordings archive link in Channels.

```
POST https://connect.mindcloud.co/v1/universal/channels/latest/actions/create-recordings-archive-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/channels/latest/actions/create-recordings-archive-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dateFrom": "2026-05-07T12:00:00.000Z",
  "dateTo": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channels/latest/actions/create-recordings-archive-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dateFrom": "2026-05-07T12:00:00.000Z",
    "dateTo": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateFrom` | date | yes | Lower bound for call recordings to include in the archive. |
| `dateTo` | date | yes | Upper bound for call recordings to include in the archive. |
| `msisdns[]` | array<string> | no | Optional phone numbers to include in the recordings archive. Accepts multiple values as an array. |
| `userIds[]` | array<number> | no | Optional user IDs participating in calls to include in the archive. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateFrom": "2026-05-07T12:00:00.000Z",
      "dateTo": "2026-05-07T12:00:00.000Z",
      "link": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateFrom` | date |  |
| `dateTo` | date |  |
| `link` | string |  |

## Native endpoint

Through the native Channels API, this operation is `POST /api/v1/archive` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recordings-archive-link.md) for the provider-specific parameters and requirements.

