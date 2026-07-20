# OnlineCheckWriter: Get Wallet

Retrieves details for a specific wallet.

```
GET https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-wallet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-wallet?connectionId=$CONNECTION_ID&walletId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "walletId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-wallet?${params}`, {
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
| `walletId` | string | yes | The wallet identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "availableBalance": "string",
        "bankAccountId": {},
        "bankAccountName": {},
        "bankAccountNatureType": {},
        "bankAccountNickName": {},
        "bankAccountNumber": "string",
        "currentBalance": "string",
        "id": "string",
        "walletName": "Ava Chen",
        "walletType": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.availableBalance` | string |  |
| `data.bankAccountId` | object |  |
| `data.bankAccountName` | object |  |
| `data.bankAccountNatureType` | object |  |
| `data.bankAccountNickName` | object |  |
| `data.bankAccountNumber` | string |  |
| `data.currentBalance` | string |  |
| `data.id` | string |  |
| `data.walletName` | string |  |
| `data.walletType` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `GET /wallet/:walletId` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet.md) for the provider-specific parameters and requirements.

