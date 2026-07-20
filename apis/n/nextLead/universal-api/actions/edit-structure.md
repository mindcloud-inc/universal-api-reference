# NextLead: Edit Structure

Updates an existing structure in NextLead.

```
PUT https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/edit-structure
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/edit-structure" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/edit-structure', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Structure identifier. |
| `email` | string | yes | Updated structure email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "structure": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `structure` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native NextLead API, this operation is `POST /api/v2/receive/structure/edit-structure` (base URL `https://dashboard.nextlead.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-structure.md) for the provider-specific parameters and requirements.

