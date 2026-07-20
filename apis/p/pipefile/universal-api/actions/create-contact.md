# Pipefile: Create Contact

Creates a new contact in Pipefile.

```
POST https://connect.mindcloud.co/v1/universal/pipefile/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipefile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipefile/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipefile/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Contact name. |
| `email` | string | no | Primary email address for the contact. |
| `phone` | string | no | Primary phone number for the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "emailBounced": true,
      "emailComplained": true,
      "name": "Ava Chen",
      "phone": "string",
      "phoneUnreachable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Primary email address for the contact. |
| `emailBounced` | boolean | Whether Pipefile marks the contact email as bounced. |
| `emailComplained` | boolean | Whether Pipefile marks the contact email as complained. |
| `name` | string | Contact name returned by Pipefile. |
| `phone` | string | Primary phone number for the contact. |
| `phoneUnreachable` | boolean | Whether Pipefile marks the contact phone as unreachable. |

## Native endpoint

Through the native Pipefile API, this operation is `POST /contacts/` (base URL `https://api.pipefile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

