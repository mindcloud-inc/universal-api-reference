# Timizer: Create Client Contact

Creates a client contact in Timizer.

```
POST https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-client-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-client-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-client-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Email address of the contact. |
| `firstname` | string | no | First name of the contact. |
| `id` | number | yes | ID of the client. |
| `lastname` | string | no | Last name of the contact. |
| `occupation` | string | no | Occupation of the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": 1,
      "lastname": "Chen",
      "occupation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstname` | string |  |
| `id` | number |  |
| `lastname` | string |  |
| `occupation` | string |  |

## Native endpoint

Through the native Timizer API, this operation is `POST /app/clients/:id/contacts` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client-contact.md) for the provider-specific parameters and requirements.

