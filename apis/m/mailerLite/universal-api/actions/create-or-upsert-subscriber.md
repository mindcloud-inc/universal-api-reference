# MailerLite: Create or Upsert Subscriber

Creates a subscriber in MailerLite, or updates one with the same email.

```
POST https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/create-or-upsert-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/create-or-upsert-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "dummy@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/create-or-upsert-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "dummy@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Subscriber email address. Example: `dummy@example.com`. |
| `fields` | object | no | Field values keyed by default or custom field name. Example: `[object Object]`. |
| `groups[]` | array<string> | no | Existing group IDs to add the subscriber to. Example: `123`. |
| `status` | string | no | Subscriber status. Example: `active`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resubscribe` | boolean | no | Resubscribe previously unsubscribed subscribers when true. Example: `true`. |
| `subscribedAt` | string | no | Subscription timestamp in yyyy-MM-dd HH:mm:ss format. Example: `2026-03-05 12:00:00`. |
| `ipAddress` | string | no | Subscriber IP address. Example: `203.0.113.10`. |
| `optedInAt` | string | no | Opt-in timestamp in yyyy-MM-dd HH:mm:ss format. Example: `2026-03-05 12:00:00`. |
| `optinIp` | string | no | Opt-in IP address. Example: `203.0.113.10`. |
| `unsubscribedAt` | string | no | Unsubscribe timestamp in yyyy-MM-dd HH:mm:ss format. Example: `2026-03-05 12:00:00`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clickRate": 1,
      "clicksCount": 1,
      "createdAt": "string",
      "email": "ava@example.com",
      "fields": {},
      "groups": [
        {}
      ],
      "id": "string",
      "ipAddress": "string",
      "openRate": 1,
      "opensCount": 1,
      "optedInAt": "string",
      "optinIp": "string",
      "sent": 1,
      "source": "string",
      "status": "string",
      "subscribedAt": "string",
      "unsubscribedAt": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clickRate` | number | Click rate percentage. |
| `clicksCount` | number | Email click count. |
| `createdAt` | string | Record creation timestamp. |
| `email` | string | Subscriber email address. |
| `fields` | object | Subscriber field values keyed by field name. |
| `groups` | array<object> | Groups attached to the subscriber. |
| `id` | string | MailerLite subscriber ID. |
| `ipAddress` | string | Subscriber IP address. |
| `openRate` | number | Open rate percentage. |
| `opensCount` | number | Email open count. |
| `optedInAt` | string | Opt-in timestamp. |
| `optinIp` | string | Opt-in IP address. |
| `sent` | number | Sent campaign count. |
| `source` | string | Subscriber source. |
| `status` | string | Subscriber status. |
| `subscribedAt` | string | Subscription timestamp. |
| `unsubscribedAt` | string | Unsubscribe timestamp. |
| `updatedAt` | string | Record update timestamp. |

## Native endpoint

Through the native MailerLite API, this operation is `POST /subscribers` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-upsert-subscriber.md) for the provider-specific parameters and requirements.

