# Torque: Get Enso Approval Transaction



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-enso-approval-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-enso-approval-transaction?connectionId=$CONNECTION_ID&fromAddress=string&tokenAddress=string&amount=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromAddress": "string",
  "tokenAddress": "string",
  "amount": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-enso-approval-transaction?${params}`, {
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
| `fromAddress` | string | yes | Wallet address that would approve token spending. |
| `tokenAddress` | string | yes | Token contract address. |
| `chainId` | number | no | Blockchain chain ID. Defaults to Ethereum mainnet when Torque provides a default. |
| `amount` | string | yes | Amount in wei. |
| `routingStrategy` | list | no | Routing strategy. Torque defaults to router. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalData": {},
      "approvalNeeded": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalData` | object |  |
| `approvalNeeded` | boolean |  |

## Native endpoint

Through the native Torque API, this operation is `POST /enso/approval` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enso-approval-transaction.md) for the provider-specific parameters and requirements.

