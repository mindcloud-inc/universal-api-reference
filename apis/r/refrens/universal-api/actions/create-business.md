# Refrens: Create Business



```
POST https://connect.mindcloud.co/v1/universal/refrens/latest/actions/create-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refrens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/create-business" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "country": "string",
  "auth": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refrens/latest/actions/create-business', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "country": "string",
    "auth": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `country` | string | yes |  |
| `auth` | object | yes | Object containing auth.email array of users to add to the business. |
| `billedTo` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "billedTo": {},
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "gstin": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "urlKey": "https://example.com",
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `billedTo` | object |  |
| `country` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `gstin` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |
| `urlKey` | string |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Refrens API, this operation is `POST /businesses` (base URL `https://api.refrens.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-business.md) for the provider-specific parameters and requirements.

