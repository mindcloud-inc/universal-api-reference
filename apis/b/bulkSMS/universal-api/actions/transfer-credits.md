# BulkSMS: Transfer Credits

Transfers credits to another BulkSMS account.

```
POST https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/transfer-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/transfer-credits" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "toUsername": "Ava Chen",
  "toUserId": 1,
  "credits": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/transfer-credits', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "toUsername": "Ava Chen",
    "toUserId": 1,
    "credits": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `toUsername` | string | yes | Username of the BulkSMS account that will receive credits. |
| `toUserId` | number | yes | Numeric user ID of the account that will receive credits. It must match the username. |
| `credits` | number | yes | Amount of credits to transfer. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commentOnFrom` | string | no | Optional note shown on the sender account credit history. |
| `commentOnTo` | string | no | Optional note shown on the recipient account credit history. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BulkSMS API returns.

## Native endpoint

Through the native BulkSMS API, this operation is `POST /credit/transfer` (base URL `https://api.bulksms.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transfer-credits.md) for the provider-specific parameters and requirements.

