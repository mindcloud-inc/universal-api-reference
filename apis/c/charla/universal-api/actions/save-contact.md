# Charla: Save Contact

Saves a contact record in Charla.

```
POST https://connect.mindcloud.co/v1/universal/charla/latest/actions/save-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Charla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/charla/latest/actions/save-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/charla/latest/actions/save-contact', {
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
| `browserLanguage` | string | no | Browser language used by the visitor. |
| `countryCode` | string | no | Country code in ISO 3166-1 format. |
| `email` | string | no | Email of the visitor if available. |
| `id` | string | no | Provide an existing contact ID to update that contact. |
| `ip` | string | no | IP address of the visitor. |
| `location` | string | no | Location of the visitor. |
| `name` | string | no | Name of the visitor if available. |
| `phone` | string | no | Phone of the visitor if available. |
| `platform` | string | no | Device or platform used by the visitor. |

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

Through the native Charla API, this operation is `POST /contacts` (base URL `https://api.charla.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-contact.md) for the provider-specific parameters and requirements.

