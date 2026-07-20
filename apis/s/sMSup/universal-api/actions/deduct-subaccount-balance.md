# SMSup: Deduct Subaccount Balance



```
PUT https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/deduct-subaccount-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/deduct-subaccount-balance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userName": "subaccount_user_name",
  "amount": "150"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/deduct-subaccount-balance', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userName": "subaccount_user_name",
    "amount": "150"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userName` | string | yes | Username of the subaccount. Example: `subaccount_user_name`. |
| `amount` | number | yes | Amount to deduct. Example: `150`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": "string",
      "currency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | string |  |
| `currency` | string |  |

## Native endpoint

Through the native SMSup API, this operation is `POST /api/3.0/subaccount/deduct-balance` (base URL `https://api.gateway360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deduct-subaccount-balance.md) for the provider-specific parameters and requirements.

