# Harvest: Create Client

Creates a new client in Harvest.

```
POST https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-client', {
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
| `name` | string | yes |  |
| `isActive` | boolean | no |  |
| `address` | string | no |  |
| `currency` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": 1,
      "isActive": true,
      "name": "Ava Chen",
      "statementKey": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `statementKey` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Harvest API, this operation is `POST /v2/clients` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

