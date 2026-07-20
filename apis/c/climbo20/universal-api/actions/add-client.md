# Climbo 2.0: Add Client

Creates a new client in Climbo 2.0.

```
POST https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/add-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Climbo 2.0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/add-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "planId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/add-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "planId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userName` | string | no | Name of the customer. |
| `email` | string | yes | Email of the customer. |
| `planId` | string | yes | Plan ID to associate to the customer. |
| `welcome` | string | no | Send welcome email to the customer with a magic link to log in. Default: `true`. |
| `password` | string | no | Must be at least 8 characters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessName": "Ava Chen",
      "createdAt": "string",
      "email": "ava@example.com",
      "id": "string",
      "locationCount": 1,
      "planId": "string",
      "source": "string",
      "status": "string",
      "userName": "Ava Chen"
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
| `id` | string |  |
| `locationCount` | number |  |
| `planId` | string |  |
| `source` | string |  |
| `status` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Climbo 2.0 API, this operation is `POST /client` (base URL `https://api.climbo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-client.md) for the provider-specific parameters and requirements.

