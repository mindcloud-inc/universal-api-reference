# ProdPad: Create Contact

Creates a new contact in ProdPad.

```
POST https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProdPad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `email` | string | yes |  |
| `about` | string | no |  |
| `phone` | string | no |  |
| `twitterUrl` | string | no |  |
| `company` | string | no |  |
| `jobRole` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "about": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "phone": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `about` | string |  |
| `created_at` | date |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native ProdPad API, this operation is `POST /contacts` (base URL `https://api.prodpad.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

