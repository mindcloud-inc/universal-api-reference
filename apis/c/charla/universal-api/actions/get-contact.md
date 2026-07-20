# Charla: Get Contact

Retrieves a contact from Charla.

```
GET https://connect.mindcloud.co/v1/universal/charla/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Charla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/charla/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/charla/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes | The contact ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browser_language": "string",
      "country_code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "ip": "string",
      "last_seen_at": "2026-05-07T12:00:00.000Z",
      "location": "string",
      "name": "Ava Chen",
      "phone": "string",
      "platform": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browser_language` | string |  |
| `country_code` | string |  |
| `created_at` | date |  |
| `email` | string |  |
| `id` | string |  |
| `ip` | string |  |
| `last_seen_at` | date |  |
| `location` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `platform` | string |  |

## Native endpoint

Through the native Charla API, this operation is `GET /contacts/:id` (base URL `https://api.charla.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

