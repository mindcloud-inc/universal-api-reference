# Lome: Create Contact

Creates a new contact in Lome.

```
POST https://connect.mindcloud.co/v1/universal/lome/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lome/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lome/latest/actions/create-contact', {
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
| `name` | string | no | Contact name. |
| `email` | string | no | Contact email address. |
| `phone` | string | no | Contact phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "home_id": "string",
      "id": "string",
      "member_id": "string",
      "name": "Ava Chen",
      "phone": "string",
      "source": "string",
      "source_id": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `email` | string |  |
| `home_id` | string |  |
| `id` | string |  |
| `member_id` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `source` | string |  |
| `source_id` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Lome API, this operation is `POST /v1/contacts` (base URL `https://grow.withlome.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

