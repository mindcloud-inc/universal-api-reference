# Signaturit: Create Contact

Creates a new contact in Signaturit.

```
POST https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Signaturit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "sandbox-contact@example.com",
  "name": "Sandbox Contact"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "sandbox-contact@example.com",
    "name": "Sandbox Contact"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email of the new contact. Example: `sandbox-contact@example.com`. |
| `name` | string | yes | Name of the new contact. Example: `Sandbox Contact`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Signaturit API, this operation is `POST /contacts.json` (base URL `https://api.sandbox.signaturit.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

