# Mailrelay: Create Sender

Creates a new sender in Mailrelay.

```
POST https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/create-sender
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/create-sender" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "apps@mindcloud.co",
  "name": "MindCloud"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/create-sender', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "apps@mindcloud.co",
    "name": "MindCloud"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Sender email address. Example: `apps@mindcloud.co`. |
| `fromName` | string | no | Displayed sender name. Example: `MindCloud Team`. |
| `name` | string | yes | Sender name. Example: `MindCloud`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confirmed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "default": true,
      "email": "ava@example.com",
      "fromName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmed` | boolean |  |
| `createdAt` | date |  |
| `default` | boolean |  |
| `email` | string |  |
| `fromName` | string |  |
| `id` | number |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Mailrelay API, this operation is `POST senders` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sender.md) for the provider-specific parameters and requirements.

