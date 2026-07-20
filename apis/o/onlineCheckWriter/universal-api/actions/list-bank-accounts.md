# OnlineCheckWriter: List Bank Accounts

Lists bank accounts in the connected OnlineCheckWriter account.

```
GET https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-bank-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-bank-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-bank-accounts?${params}`, {
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
      "data": {
        "bankAccounts": [
          {
            "accountNumber": "string",
            "addressLine1": {},
            "addressLine2": {},
            "bankAccountId": "string",
            "bankId": "string",
            "city": {},
            "createdDate": "string",
            "isAchEnabled": true,
            "isVerified": true,
            "name": "Ava Chen",
            "nickName": "Ava Chen",
            "phone": {},
            "state": {},
            "webUrl": "https://example.com",
            "zip": {}
          }
        ],
        "meta": {
          "currentPage": 1,
          "perPage": 1,
          "total": 1
        }
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
| `data.bankAccounts[].accountNumber` | string |  |
| `data.bankAccounts[].addressLine1` | object |  |
| `data.bankAccounts[].addressLine2` | object |  |
| `data.bankAccounts[].bankAccountId` | string |  |
| `data.bankAccounts[].bankId` | string |  |
| `data.bankAccounts[].city` | object |  |
| `data.bankAccounts[].createdDate` | string |  |
| `data.bankAccounts[].isAchEnabled` | boolean |  |
| `data.bankAccounts[].isVerified` | boolean |  |
| `data.bankAccounts[].name` | string |  |
| `data.bankAccounts[].nickName` | string |  |
| `data.bankAccounts[].phone` | object |  |
| `data.bankAccounts[].state` | object |  |
| `data.bankAccounts[].webUrl` | string |  |
| `data.bankAccounts[].zip` | object |  |
| `data.meta.currentPage` | number |  |
| `data.meta.perPage` | number |  |
| `data.meta.total` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `GET /bankAccounts` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bank-accounts.md) for the provider-specific parameters and requirements.

