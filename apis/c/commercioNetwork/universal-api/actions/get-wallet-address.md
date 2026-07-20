# CommercioNetwork: Get Wallet Address

Retrieves your wallet address from CommercioNetwork.

```
GET https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/get-wallet-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CommercioNetwork `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_number` | string | The wallet account number. |
| `address` | string | The wallet DID address. |
| `coins` | array<object> | The wallet token balances. |
| `public_key` | object | The wallet public key payload when present. |
| `sequence` | string | The wallet sequence. |

## Native endpoint

Through the native CommercioNetwork API, this operation is `GET /wallet/address` (base URL `https://dev-api.commercio.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet-address.md) for the provider-specific parameters and requirements.

