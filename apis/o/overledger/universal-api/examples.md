# Overledger Universal API Examples

These examples use the MindCloud API key and Overledger connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Supported Fungible Tokens



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/overledger/latest/actions/list-supported-fungible-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/overledger/latest/actions/list-supported-fungible-tokens?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "contractType": "string",
      "decimalPlaces": 1,
      "documentationUrl": "https://example.com",
      "functions": [
        {}
      ],
      "location": {},
      "smartContractId": "string",
      "unit": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Supported Fungible Tokens action reference](actions/list-supported-fungible-tokens.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/overledger/latest/actions/list-supported-fungible-tokens).

## Create Smart Contract Webhook



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

Example response:

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

See the full [Create Smart Contract Webhook action reference](actions/create-smart-contract-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/overledger/latest/actions/create-smart-contract-webhook).
