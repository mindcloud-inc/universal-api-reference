# Mailrelay: Get Subscriber

Retrieves subscriber details from your Mailrelay account.

```
GET https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/get-subscriber?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/get-subscriber?${params}`, {
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
| `id` | number | yes | The Mailrelay subscriber ID. Example: `1`. |

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

Through the native Mailrelay API, this operation is `GET subscribers/:id` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber.md) for the provider-specific parameters and requirements.

