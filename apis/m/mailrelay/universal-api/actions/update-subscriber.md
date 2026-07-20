# Mailrelay: Update Subscriber

Updates an existing subscriber in Mailrelay.

```
PUT https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/update-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/update-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/update-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `country` | string | no | Updated subscriber country in ISO 3166-1 alpha-2 format. Example: `US`. |
| `groupIds[]` | array<number> | no | Updated group IDs for the subscriber. Example: `2`. |
| `id` | number | yes | The Mailrelay subscriber ID. Example: `1`. |
| `locale` | string | no | Updated subscriber locale. |
| `name` | string | no | Updated subscriber name. |
| `smsPhone` | string | no | Updated subscriber SMS phone number. |
| `timeZone` | string | no | Updated subscriber time zone. |
| `whatsappPhone` | string | no | Updated subscriber WhatsApp phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "birthday": "2026-05-07T12:00:00.000Z",
      "bounceCategory": "string",
      "bounced": true,
      "city": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "email": "ava@example.com",
      "globalBan": true,
      "groups": [
        {}
      ],
      "id": 1,
      "localBan": true,
      "locale": "string",
      "name": "Ava Chen",
      "reportedSpam": true,
      "score": 1,
      "smsPhone": "string",
      "smsStatus": "string",
      "state": "string",
      "status": "string",
      "subscribedAt": "2026-05-07T12:00:00.000Z",
      "subscribedWithAcceptance": true,
      "subscribeIp": "string",
      "timeZone": "string",
      "unsubscribed": true,
      "unsubscribedAt": "2026-05-07T12:00:00.000Z",
      "unsubscribeIp": "string",
      "unsubscribeSentEmailId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "website": "string",
      "whatsappPhone": "string",
      "whatsappStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `birthday` | date |  |
| `bounceCategory` | string |  |
| `bounced` | boolean |  |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | date |  |
| `customFields` | object |  |
| `email` | string |  |
| `globalBan` | boolean |  |
| `groups` | array<object> |  |
| `id` | number |  |
| `localBan` | boolean |  |
| `locale` | string |  |
| `name` | string |  |
| `reportedSpam` | boolean |  |
| `score` | number |  |
| `smsPhone` | string |  |
| `smsStatus` | string |  |
| `state` | string |  |
| `status` | string |  |
| `subscribedAt` | date |  |
| `subscribedWithAcceptance` | boolean |  |
| `subscribeIp` | string |  |
| `timeZone` | string |  |
| `unsubscribed` | boolean |  |
| `unsubscribedAt` | date |  |
| `unsubscribeIp` | string |  |
| `unsubscribeSentEmailId` | number |  |
| `updatedAt` | date |  |
| `website` | string |  |
| `whatsappPhone` | string |  |
| `whatsappStatus` | string |  |

## Native endpoint

Through the native Mailrelay API, this operation is `PATCH subscribers/:id` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber.md) for the provider-specific parameters and requirements.

