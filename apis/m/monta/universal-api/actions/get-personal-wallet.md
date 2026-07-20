# Monta: Get Personal Wallet

Retrieves your personal team wallet from Monta.

```
GET https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-personal-wallet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-personal-wallet?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-personal-wallet?${params}`, {
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
      "balance": {
        "amount": 1,
        "credit": 1
      },
      "currency": {
        "decimals": 1,
        "identifier": "string",
        "name": "Ava Chen"
      },
      "id": 1,
      "ownerId": 1,
      "ownerType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance.amount` | number |  |
| `balance.credit` | number |  |
| `currency.decimals` | number |  |
| `currency.identifier` | string |  |
| `currency.name` | string |  |
| `id` | number |  |
| `ownerId` | number |  |
| `ownerType` | string |  |

## Native endpoint

Through the native Monta API, this operation is `GET /wallets/personal` (base URL `https://public-api.monta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-personal-wallet.md) for the provider-specific parameters and requirements.

