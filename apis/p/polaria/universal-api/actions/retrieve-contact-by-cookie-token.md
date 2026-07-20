# Polaria: Retrieve Contact by Cookie Token

Retrieves a contact from Polaria by cookie token.

```
GET https://connect.mindcloud.co/v1/universal/polaria/latest/actions/retrieve-contact-by-cookie-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polaria `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polaria/latest/actions/retrieve-contact-by-cookie-token?connectionId=$CONNECTION_ID&apiKey=string&cookieToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apiKey": "string",
  "cookieToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polaria/latest/actions/retrieve-contact-by-cookie-token?${params}`, {
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
| `apiKey` | string | yes |  |
| `cookieToken` | string | yes |  |

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

Through the native Polaria API, this operation is `GET /widgets/[:api_key]/contacts/retrieve` (base URL `https://app.polaria.ai/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact-by-cookie-token.md) for the provider-specific parameters and requirements.

