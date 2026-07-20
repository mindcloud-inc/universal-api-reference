# Poof: Create Wallet

Creates a new wallet in Poof.

```
POST https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-a-wallet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-a-wallet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currency": "polygon"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-a-wallet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currency": "polygon"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currency` | string | yes | Wallet currency or chain. Default: `polygon`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Poof API returns.

## Native endpoint

Through the native Poof API, this operation is `POST https://www.poof.io/api/v2/create_wallet` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-wallet.md) for the provider-specific parameters and requirements.

