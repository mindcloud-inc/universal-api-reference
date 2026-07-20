# Mailrelay: Send Campaign

Sends a Mailrelay campaign to its selected audience.

```
POST https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/send-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/send-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1",
  "target": "groups"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/send-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1",
    "target": "groups"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | Webhook URL to notify after the campaign is sent. |
| `groupIds[]` | array<number> | no | Group IDs when target is `groups`. Example: `1,2`. |
| `id` | number | yes | The Mailrelay campaign ID. Example: `1`. |
| `scheduledAt` | string | no | UTC send time in `YYYY-MM-DD HH:MM:SS` format. |
| `segmentId` | number | no | Segment ID when target is `segment`. Example: `12`. |
| `target` | list | yes | Who the campaign should be sent to. One of: `0`, `1`. Example: `groups`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "html": "string",
      "id": 1,
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "senderId": 1,
      "status": "string",
      "subject": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string |  |
| `createdAt` | date |  |
| `html` | string |  |
| `id` | number |  |
| `scheduledAt` | date |  |
| `senderId` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Mailrelay API, this operation is `POST campaigns/:id/send_all` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-campaign.md) for the provider-specific parameters and requirements.

