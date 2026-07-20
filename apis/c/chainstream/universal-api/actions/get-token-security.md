# Chainstream: Get Token Security

Retrieves token security details from Chainstream.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-token-security
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-token-security?connectionId=$CONNECTION_ID&chain=string&tokenAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string",
  "tokenAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-token-security?${params}`, {
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
| `chain` | string | yes | Supported blockchain chain |
| `tokenAddress` | string | yes | Token contract address |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance_mutable_authority": {},
      "closable": {},
      "creators": [
        {}
      ],
      "default_account_state": "string",
      "default_account_state_upgradable": {},
      "dex": [
        {}
      ],
      "freezable": {},
      "holder_count": "string",
      "holders": [
        {}
      ],
      "lp_holders": [
        {}
      ],
      "metadata": {},
      "metadata_mutable": {},
      "mintable": {},
      "non_transferable": "string",
      "total_supply": "string",
      "transfer_fee": {},
      "transfer_fee_upgradable": {},
      "transfer_hook": [
        {}
      ],
      "transfer_hook_upgradable": {},
      "trusted_token": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance_mutable_authority` | object |  |
| `closable` | object |  |
| `creators` | array<object> |  |
| `default_account_state` | string |  |
| `default_account_state_upgradable` | object |  |
| `dex` | array<object> |  |
| `freezable` | object |  |
| `holder_count` | string |  |
| `holders` | array<object> |  |
| `lp_holders` | array<object> |  |
| `metadata` | object |  |
| `metadata_mutable` | object |  |
| `mintable` | object |  |
| `non_transferable` | string |  |
| `total_supply` | string |  |
| `transfer_fee` | object |  |
| `transfer_fee_upgradable` | object |  |
| `transfer_hook` | array<object> |  |
| `transfer_hook_upgradable` | object |  |
| `trusted_token` | number |  |

## Native endpoint

Through the native Chainstream API, this operation is `GET /v2/token/:chain/:tokenAddress/security` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-security.md) for the provider-specific parameters and requirements.

