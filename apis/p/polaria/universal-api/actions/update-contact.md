# Polaria: Update Contact

Updates an existing contact in Polaria.

```
PUT https://connect.mindcloud.co/v1/universal/polaria/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polaria `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/polaria/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "apiKey": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/polaria/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "apiKey": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiKey` | string | yes | The Polaria widget API key for the target brand. |
| `id` | string | yes | The ID of the contact to update. |
| `email` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browser": "string",
      "city": "string",
      "cookieToken": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "from": "string",
      "id": 1,
      "ip": "string",
      "language": "string",
      "lastMessageAt": "2026-05-07T12:00:00.000Z",
      "latitude": 1,
      "longitude": 1,
      "more": {},
      "name": "Ava Chen",
      "platform": "string",
      "referrer": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browser` | string |  |
| `city` | string |  |
| `cookieToken` | string |  |
| `country` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `from` | string |  |
| `id` | number |  |
| `ip` | string |  |
| `language` | string |  |
| `lastMessageAt` | date |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `more` | object |  |
| `name` | string |  |
| `platform` | string |  |
| `referrer` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `zipcode` | string |  |

## Native endpoint

Through the native Polaria API, this operation is `PUT /widgets/[:api_key]/contacts/[:id]` (base URL `https://app.polaria.ai/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

