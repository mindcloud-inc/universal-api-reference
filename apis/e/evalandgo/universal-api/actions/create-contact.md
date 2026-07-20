# Evalandgo: Create Contact

Creates a new contact in Evalandgo.

```
POST https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-contact', {
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
| `email` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `phone` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | no |  |
| `password` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "createAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "hasPassword": true,
      "id": 1,
      "lastName": "Chen",
      "optinAt": "string",
      "phone": "string",
      "status": {},
      "username": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `@type` | string |  |
| `createAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `hasPassword` | boolean |  |
| `id` | number |  |
| `lastName` | string |  |
| `optinAt` | string |  |
| `phone` | string |  |
| `status` | object |  |
| `username` | object |  |

## Native endpoint

Through the native Evalandgo API, this operation is `POST /api/v3/contacts` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

