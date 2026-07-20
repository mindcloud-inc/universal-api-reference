# Paymo: Create Client

Creates a client in Paymo.

```
POST https://connect.mindcloud.co/v1/universal/paymo/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paymo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paymo/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paymo/latest/actions/create-client', {
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
| `name` | string | no |  |
| `name` | string | yes | The client name. |
| `email` | string | no |  |
| `email` | string | no | The client email address. |
| `phone` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "address": "string",
      "city": "string",
      "country": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "dueInterval": 1,
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "postalCode": "string",
      "state": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `address` | string |  |
| `city` | string |  |
| `country` | string |  |
| `createdOn` | date |  |
| `dueInterval` | number |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `postalCode` | string |  |
| `state` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Paymo API, this operation is `POST clients` (base URL `https://app.paymoapp.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

