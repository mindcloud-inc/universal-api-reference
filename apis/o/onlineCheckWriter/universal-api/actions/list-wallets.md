# OnlineCheckWriter: List Wallets

Lists wallets available in the connected OnlineCheckWriter account.

```
GET https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-wallets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-wallets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-wallets?${params}`, {
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
      "data": [
        {
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
        }
      ],
      "meta": {
        "currentPage": 1,
        "lastPage": 1,
        "perPage": 1,
        "total": 1
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
| `data[].availableBalance` | string |  |
| `data[].bankAccountId` | object |  |
| `data[].bankAccountName` | object |  |
| `data[].bankAccountNatureType` | object |  |
| `data[].bankAccountNickName` | object |  |
| `data[].bankAccountNumber` | string |  |
| `data[].currentBalance` | string |  |
| `data[].id` | string |  |
| `data[].walletName` | string |  |
| `data[].walletType` | number |  |
| `meta.currentPage` | number |  |
| `meta.lastPage` | number |  |
| `meta.perPage` | number |  |
| `meta.total` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `GET /wallet/` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-wallets.md) for the provider-specific parameters and requirements.

