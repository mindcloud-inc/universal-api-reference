# Prembly: Bank Account (Basic)

Creates a basic bank account verification in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/bank-account-basic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/bank-account-basic" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/bank-account-basic', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "account_data": {
        "account_name": "Ava Chen",
        "account_number": "string"
      },
      "detail": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_data.account_name` | string |  |
| `account_data.account_number` | string |  |
| `detail` | string |  |
| `status` | boolean |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /verification/bank_account/basic` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bank-account-basic.md) for the provider-specific parameters and requirements.

