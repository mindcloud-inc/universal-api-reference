# WhatsScale: List WhatsApp Contacts

Retrieves WhatsApp contacts from a WhatsScale session.

```
GET https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/list-whats-app-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsScale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/list-whats-app-contacts?connectionId=$CONNECTION_ID&session=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "session": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/list-whats-app-contacts?${params}`, {
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
| `session` | string | yes | Session name from /api/sessions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "pushName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `pushName` | string |  |

## Native endpoint

Through the native WhatsScale API, this operation is `GET /api/:session/contacts` (base URL `https://proxy.whatsscale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-whats-app-contacts.md) for the provider-specific parameters and requirements.

