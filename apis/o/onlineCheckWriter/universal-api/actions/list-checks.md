# OnlineCheckWriter: List Checks

Lists checks in the connected OnlineCheckWriter account.

```
GET https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-checks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-checks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-checks?${params}`, {
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
        "checks": [
          {
            "accountNumber": "string",
            "amount": "string",
            "amountInWord": "string",
            "bankAccount": {
              "bankAccountId": "string",
              "name": "Ava Chen"
            },
            "category": {
              "categoryId": "string",
              "name": {}
            },
            "checkId": "string",
            "checkStatus": {
              "description": "string",
              "status": 1
            },
            "date": "string",
            "invoiceNumber": "string",
            "memo": "string",
            "note": "string",
            "payee": {
              "name": {},
              "payeeId": "string"
            },
            "referenceId": {},
            "serialNumber": "string",
            "status": 1
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
| `data.checks[].accountNumber` | string |  |
| `data.checks[].amount` | string |  |
| `data.checks[].amountInWord` | string |  |
| `data.checks[].bankAccount.bankAccountId` | string |  |
| `data.checks[].bankAccount.name` | string |  |
| `data.checks[].category.categoryId` | string |  |
| `data.checks[].category.name` | object |  |
| `data.checks[].checkId` | string |  |
| `data.checks[].checkStatus.description` | string |  |
| `data.checks[].checkStatus.status` | number |  |
| `data.checks[].date` | string |  |
| `data.checks[].invoiceNumber` | string |  |
| `data.checks[].memo` | string |  |
| `data.checks[].note` | string |  |
| `data.checks[].payee.name` | object |  |
| `data.checks[].payee.payeeId` | string |  |
| `data.checks[].referenceId` | object |  |
| `data.checks[].serialNumber` | string |  |
| `data.checks[].status` | number |  |
| `data.meta.currentPage` | number |  |
| `data.meta.perPage` | number |  |
| `data.meta.total` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `GET /checks` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-checks.md) for the provider-specific parameters and requirements.

