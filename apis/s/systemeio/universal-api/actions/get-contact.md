# Systeme.io: Get Contact

Retrieves a contact resource from Systeme.io.

```
GET https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes | Contact identifier |

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
| `id` | number | Contact ID. |
| `locale` | string | Contact locale. |
| `needsConfirmation` | boolean | Needs confirmation state. |
| `registeredAt` | date | Contact registration timestamp. |
| `sourceURL` | string | Contact source URL if present. |
| `tags` | array<object> | Assigned tags. |
| `unsubscribed` | boolean | Unsubscribed state. |

## Native endpoint

Through the native Systeme.io API, this operation is `GET /api/contacts/:id` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

