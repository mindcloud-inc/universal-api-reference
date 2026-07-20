# OnlineCheckWriter: List Payees

Lists payees in the connected OnlineCheckWriter account.

```
GET https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-payees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-payees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-payees?${params}`, {
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
        "meta": {
          "currentPage": 1,
          "perPage": 1,
          "total": 1
        },
        "payees": [
          {
            "address1": "string",
            "address2": "string",
            "city": "string",
            "company": "string",
            "country": {},
            "dob": {},
            "email": {},
            "entityType": {},
            "name": "Ava Chen",
            "nickName": {},
            "payeeId": "string",
            "phone": {},
            "state": "string",
            "zip": "string"
          }
        ]
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
| `data.meta.currentPage` | number |  |
| `data.meta.perPage` | number |  |
| `data.meta.total` | number |  |
| `data.payees[].address1` | string |  |
| `data.payees[].address2` | string |  |
| `data.payees[].city` | string |  |
| `data.payees[].company` | string |  |
| `data.payees[].country` | object |  |
| `data.payees[].dob` | object |  |
| `data.payees[].email` | object |  |
| `data.payees[].entityType` | object |  |
| `data.payees[].name` | string |  |
| `data.payees[].nickName` | object |  |
| `data.payees[].payeeId` | string |  |
| `data.payees[].phone` | object |  |
| `data.payees[].state` | string |  |
| `data.payees[].zip` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `GET /payees` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payees.md) for the provider-specific parameters and requirements.

