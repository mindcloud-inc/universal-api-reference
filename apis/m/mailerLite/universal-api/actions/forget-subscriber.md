# MailerLite: Forget Subscriber

Deletes a subscriber from MailerLite and permanently removes their data.

```
DELETE https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/forget-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/forget-subscriber?connectionId=$CONNECTION_ID&id=180863157267334516" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "180863157267334516"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/forget-subscriber?${params}`, {
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
| `id` | string | yes | Subscriber ID for the account. Example: `180863157267334516`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clickRate": 1,
      "clicksCount": 1,
      "createdAt": "string",
      "deletedAt": "string",
      "email": "ava@example.com",
      "fields": {},
      "forgetAt": "string",
      "groups": [
        {}
      ],
      "id": "string",
      "ipAddress": "string",
      "location": {},
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
| `deletedAt` | string | Deletion timestamp. |
| `email` | string | Subscriber email address. |
| `fields` | object | Subscriber field values keyed by field name. |
| `forgetAt` | string | Data erasure completion timestamp. |
| `groups` | array<object> | Groups attached to the subscriber. |
| `id` | string | MailerLite subscriber ID. |
| `ipAddress` | string | Subscriber IP address. |
| `location` | object | Resolved subscriber location data when available. |
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

Through the native MailerLite API, this operation is `POST /subscribers/:id/forget` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/forget-subscriber.md) for the provider-specific parameters and requirements.

