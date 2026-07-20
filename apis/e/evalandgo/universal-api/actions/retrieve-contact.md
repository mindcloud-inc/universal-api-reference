# Evalandgo: Retrieve Contact

Retrieves a contact from Evalandgo.

```
GET https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-contact?${params}`, {
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

Through the native Evalandgo API, this operation is `GET /api/v3/contacts/:id` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact.md) for the provider-specific parameters and requirements.

