# Callingly: Create Client

Creates a client in Callingly.

```
POST https://connect.mindcloud.co/v1/universal/callingly/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "MindCloud",
  "lastName": "Client",
  "company": "MindCloud Test Client",
  "email": "mindcloud-callingly-client@example.com",
  "phoneNumber": "+15005550007"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callingly/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "MindCloud",
    "lastName": "Client",
    "company": "MindCloud Test Client",
    "email": "mindcloud-callingly-client@example.com",
    "phoneNumber": "+15005550007"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | Example: `MindCloud`. |
| `lastName` | string | yes | Example: `Client`. |
| `company` | string | yes | Example: `MindCloud Test Client`. |
| `email` | string | yes | Example: `mindcloud-callingly-client@example.com`. |
| `phoneNumber` | string | yes | Example: `+15005550007`. |
| `password` | string | no | Example: `MindCloud123!`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billing_email": "ava@example.com",
      "id": 1,
      "is_active": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing_email` | string |  |
| `id` | number |  |
| `is_active` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Callingly API, this operation is `POST /v1/clients` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

