# Systeme.io: Create Contact

Creates a new contact in Systeme.io.

```
POST https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Contact email address. |
| `fields[].slug` | string | no | Custom field slug. |
| `fields[].value` | string | no | Custom field value. |
| `locale` | string | no | Contact locale code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounced": true,
      "email": "ava@example.com",
      "fields": [
        {}
      ],
      "id": 1,
      "locale": "string",
      "needsConfirmation": true,
      "registeredAt": "2026-05-07T12:00:00.000Z",
      "sourceURL": "https://example.com",
      "tags": [
        {}
      ],
      "unsubscribed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounced` | boolean | Bounced state. |
| `email` | string | Contact email. |
| `fields` | array<object> | Contact custom fields. |
| `id` | number | Created contact ID. |
| `locale` | string | Contact locale. |
| `needsConfirmation` | boolean | Needs confirmation state. |
| `registeredAt` | date | Contact registration timestamp. |
| `sourceURL` | string | Contact source URL if present. |
| `tags` | array<object> | Assigned tags. |
| `unsubscribed` | boolean | Unsubscribed state. |

## Native endpoint

Through the native Systeme.io API, this operation is `POST /api/contacts` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

