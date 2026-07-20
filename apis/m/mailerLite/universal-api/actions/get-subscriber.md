# MailerLite: Get Subscriber

Retrieves a subscriber from MailerLite by ID or email.

```
GET https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/get-subscriber?connectionId=$CONNECTION_ID&idOrEmail=dummy%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrEmail": "dummy@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/get-subscriber?${params}`, {
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
| `idOrEmail` | string | yes | Subscriber ID or email address to fetch. Example: `dummy@example.com`. |

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

Through the native MailerLite API, this operation is `GET /subscribers/:idOrEmail` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber.md) for the provider-specific parameters and requirements.

