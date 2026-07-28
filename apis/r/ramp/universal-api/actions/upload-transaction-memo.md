# Ramp: Upload a new memo for a transaction



```
PUT https://connect.mindcloud.co/v1/universal/ramp/latest/actions/upload-transaction-memo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ramp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ramp/latest/actions/upload-transaction-memo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "memo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ramp/latest/actions/upload-transaction-memo', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "memo": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionId` | string | no |  |
| `memo` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "memo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `memo` | string |  |

## Native endpoint

Through the native Ramp API, this operation is `POST memos/:transactionId` (base URL `https://api.ramp.com/developer/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-transaction-memo.md) for the provider-specific parameters and requirements.

