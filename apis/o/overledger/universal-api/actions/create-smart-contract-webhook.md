# Overledger: Create Smart Contract Webhook



```
POST https://connect.mindcloud.co/v1/universal/overledger/latest/actions/create-smart-contract-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Overledger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/overledger/latest/actions/create-smart-contract-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "location": {
    "network": "ethereum sepolia testnet",
    "technology": "ethereum"
  },
  "callbackUrl": "https://example.com",
  "smartContractId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/overledger/latest/actions/create-smart-contract-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "location": {"network":"ethereum sepolia testnet","technology":"ethereum"},
    "callbackUrl": "https://example.com",
    "smartContractId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `location` | object | yes | Overledger location object with technology and network. Default: `{"network":"ethereum sepolia testnet","technology":"ethereum"}`. |
| `callbackUrl` | string | yes | Public callback URL that Overledger will send webhook events to. |
| `smartContractId` | string | yes | Smart contract identifier/address to monitor. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackUrl": "https://example.com",
      "callbackUrlStatus": "https://example.com",
      "location": {},
      "smartContractId": "string",
      "webhookId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string | Callback URL. |
| `callbackUrlStatus` | string | Callback URL status. |
| `location` | object | Blockchain location. |
| `smartContractId` | string | Monitored smart contract identifier. |
| `webhookId` | string | Created webhook identifier. |

## Native endpoint

Through the native Overledger API, this operation is `POST /api/webhooks/smart-contract-events` (base URL `https://api.overledger.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-smart-contract-webhook.md) for the provider-specific parameters and requirements.

