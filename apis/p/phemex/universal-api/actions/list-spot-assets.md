# Phemex: List Spot Assets



```
GET https://connect.mindcloud.co/v1/universal/phemex/latest/actions/list-spot-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phemex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phemex/latest/actions/list-spot-assets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phemex/latest/actions/list-spot-assets?${params}`, {
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
      "": [
        {
          "balanceEv": 1,
          "currency": "string",
          "lastUpdateTimeNs": 1,
          "lockedTradingBalanceEv": 1,
          "lockedWithdrawEv": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].balanceEv` | number |  |
| `[].currency` | string |  |
| `[].lastUpdateTimeNs` | number |  |
| `[].lockedTradingBalanceEv` | number |  |
| `[].lockedWithdrawEv` | number |  |

## Native endpoint

Through the native Phemex API, this operation is `GET /spot/wallets` (base URL `https://api.phemex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spot-assets.md) for the provider-specific parameters and requirements.

