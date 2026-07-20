# Content Snare: Create Client

Creates a client in Content Snare.

```
POST https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "fullName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "fullName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientCompanies[]` | array<object> | no | Client Companies. |
| `clientCompanies[].name` | string | no | Company name |
| `email` | string | yes | Contact email address |
| `fullName` | string | yes | Contact full name |
| `firstName` | string | no | Contact first name |
| `lastName` | string | no | Contact last name |
| `phone` | string | no | Phone number |
| `languageCode` | string | no | Language code |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "client_companies": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "company_name": "Ava Chen",
      "email": "ava@example.com",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "id": "string",
      "language_code": "string",
      "last_name": "Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `client_companies[].id` | string |  |
| `client_companies[].name` | string |  |
| `company_name` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `id` | string |  |
| `language_code` | string |  |
| `last_name` | string |  |
| `phone` | string |  |

## Native endpoint

Through the native Content Snare API, this operation is `POST /partner_api/v1/clients` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

