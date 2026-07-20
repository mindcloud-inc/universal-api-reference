# CoinGate: Get Withdrawal

Retrieves a withdrawal from CoinGate by ID.

```
GET https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-withdrawal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-withdrawal?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-withdrawal?${params}`, {
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
| `id` | number | yes | CoinGate withdrawal ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `id` | number |  |
| `status` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `GET /withdrawals/:id` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-withdrawal.md) for the provider-specific parameters and requirements.

