# Prembly: Account with Name Comparism

Creates account name comparism verification in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/account-with-name-comparism
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/account-with-name-comparism" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/account-with-name-comparism', {
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
        "account_number": "string",
        "bank_id": 1
      },
      "comparism_data": {
        "confidence": 1,
        "status": true
      },
      "detail": "string",
      "response_code": "string",
      "status": true,
      "verification": {
        "endpoint": "string",
        "reference": "string",
        "status": "string"
      }
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
| `account_data.bank_id` | number |  |
| `comparism_data.confidence` | number |  |
| `comparism_data.status` | boolean |  |
| `detail` | string |  |
| `response_code` | string |  |
| `status` | boolean |  |
| `verification.endpoint` | string |  |
| `verification.reference` | string |  |
| `verification.status` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /verification/bank_account/comparism` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/account-with-name-comparism.md) for the provider-specific parameters and requirements.

