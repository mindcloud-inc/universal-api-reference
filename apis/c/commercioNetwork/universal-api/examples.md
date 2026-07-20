# CommercioNetwork Universal API Examples

These examples use the MindCloud API key and CommercioNetwork connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Wallet Address

Retrieves your wallet address from CommercioNetwork.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-wallet-address?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-wallet-address?${params}`, {
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
      "account_number": "string",
      "address": "string",
      "coins": [
        {}
      ],
      "public_key": {},
      "sequence": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Wallet Address action reference](actions/get-wallet-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/commercioNetwork/latest/actions/get-wallet-address).

## Create Receipt

Creates a receipt process in CommercioNetwork.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/create-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentTxHash": "CDE319A5...",
  "documentUuid": "41a2b679-..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/create-receipt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentTxHash": "CDE319A5...",
    "documentUuid": "41a2b679-..."
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
      "created_at": "string",
      "document_tx_hash": "string",
      "document_uuid": "string",
      "process_id": "string",
      "recipient": "string",
      "sender": "string",
      "status": "string",
      "tx_type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Receipt action reference](actions/create-receipt.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/commercioNetwork/latest/actions/create-receipt).
