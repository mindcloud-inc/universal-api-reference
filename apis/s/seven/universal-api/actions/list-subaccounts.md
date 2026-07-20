# Seven: List Subaccounts

Retrieves subaccounts from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-subaccounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-subaccounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-subaccounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | no | The ID of a subaccount. This will give you only the data for a specific subaccount. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_topup": {
        "amount": "string",
        "threshold": "string"
      },
      "balance": "string",
      "company": "string",
      "contact": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "id": "string",
      "total_usage": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_topup` | object |  |
| `auto_topup.amount` | string |  |
| `auto_topup.threshold` | string |  |
| `balance` | string |  |
| `company` | string |  |
| `contact` | object |  |
| `contact.email` | string |  |
| `contact.name` | string |  |
| `id` | string |  |
| `total_usage` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Seven API, this operation is `GET /subaccounts?action=read` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subaccounts.md) for the provider-specific parameters and requirements.

