# Seven: Create Subaccount

Creates a new subaccount in Seven.

```
POST https://connect.mindcloud.co/v1/universal/seven/latest/actions/create-subaccount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seven/latest/actions/create-subaccount" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seven/latest/actions/create-subaccount', {
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
| `name` | string | yes | Full first and last name of the account owner. |
| `email` | string | yes | Email address of the account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "subaccount": {
        "auto_topup": {
          "amount": 1,
          "threshold": 1
        },
        "balance": 1,
        "company": "string",
        "contact": {
          "email": "ava@example.com",
          "name": "Ava Chen"
        },
        "id": "string",
        "total_usage": 1,
        "username": "Ava Chen"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `subaccount` | object |  |
| `subaccount.auto_topup` | object |  |
| `subaccount.auto_topup.amount` | number |  |
| `subaccount.auto_topup.threshold` | number |  |
| `subaccount.balance` | number |  |
| `subaccount.company` | string |  |
| `subaccount.contact` | object |  |
| `subaccount.contact.email` | string |  |
| `subaccount.contact.name` | string |  |
| `subaccount.id` | string |  |
| `subaccount.total_usage` | number |  |
| `subaccount.username` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Seven API, this operation is `POST /subaccounts?action=create` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subaccount.md) for the provider-specific parameters and requirements.

