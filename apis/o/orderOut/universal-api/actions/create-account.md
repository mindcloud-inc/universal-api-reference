# OrderOut: Create Account

Creates an account in OrderOut.

```
POST https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/create-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OrderOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountManagerEmail": "ava@example.com",
  "accountManagerFirstname": "Ava",
  "accountManagerLastname": "Chen",
  "accountManagerPhone": "string",
  "accountName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountManagerEmail": "ava@example.com",
    "accountManagerFirstname": "Ava",
    "accountManagerLastname": "Chen",
    "accountManagerPhone": "string",
    "accountName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountManagerEmail` | string | yes | Account manager email |
| `accountManagerFirstname` | string | yes | Account manager first name |
| `accountManagerLastname` | string | yes | Account manager last name |
| `accountManagerPhone` | string | yes | Account manager phone |
| `accountName` | string | yes | Account name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native OrderOut API, this operation is `POST /api/pos/account` (base URL `https://api.orderout.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account.md) for the provider-specific parameters and requirements.

