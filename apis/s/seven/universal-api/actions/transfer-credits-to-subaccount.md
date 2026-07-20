# Seven: Transfer Credits to Subaccount

Creates a subaccount credit transfer in Seven.

```
POST https://connect.mindcloud.co/v1/universal/seven/latest/actions/transfer-credits-to-subaccount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seven/latest/actions/transfer-credits-to-subaccount" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seven/latest/actions/transfer-credits-to-subaccount', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the subaccount. |
| `amount` | number | yes | Credit to be transferred. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
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
| `success` | boolean |  |

## Native endpoint

Through the native Seven API, this operation is `POST /subaccounts?action=transfer_credits` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transfer-credits-to-subaccount.md) for the provider-specific parameters and requirements.

