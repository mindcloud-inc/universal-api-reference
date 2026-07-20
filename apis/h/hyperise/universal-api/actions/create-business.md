# Hyperise: Create Business

Creates a new business in Hyperise.

```
POST https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/create-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/create-business" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessName": "Ava Chen",
  "email": "ava@example.com",
  "website": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/create-business', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessName": "Ava Chen",
    "email": "ava@example.com",
    "website": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessName` | string | yes | The business name. |
| `email` | string | yes | The business contact email. |
| `website` | string | yes | The business website. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessName": "Ava Chen",
      "createdAt": "string",
      "email": "ava@example.com",
      "id": 1,
      "updatedAt": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessName` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `id` | number |  |
| `updatedAt` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Hyperise API, this operation is `POST /businesses` (base URL `https://app.hyperise.io/api/v1/regular`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-business.md) for the provider-specific parameters and requirements.

