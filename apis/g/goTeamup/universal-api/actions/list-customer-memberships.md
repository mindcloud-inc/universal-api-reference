# GoTeamup: List Customer Memberships

Finds customer memberships in GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-customer-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-customer-memberships?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-customer-memberships?${params}`, {
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
      "count": 1,
      "next": {},
      "previous": {},
      "results": [
        {
          "activeHold": {},
          "billedPrice": {},
          "cancellationReason": {},
          "customer": 1,
          "discountCode": {},
          "discountCodeMakesFreeForever": true,
          "expirationDate": {},
          "id": 1,
          "isSetForCancellation": true,
          "membership": 1,
          "name": "Ava Chen",
          "object": "string",
          "paymentSubscription": {},
          "renewalDate": {},
          "startDate": "string",
          "status": "string"
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
| `count` | number |  |
| `next` | object |  |
| `previous` | object |  |
| `results[].activeHold` | object |  |
| `results[].billedPrice` | object |  |
| `results[].cancellationReason` | object |  |
| `results[].customer` | number |  |
| `results[].discountCode` | object |  |
| `results[].discountCodeMakesFreeForever` | boolean |  |
| `results[].expirationDate` | object |  |
| `results[].id` | number |  |
| `results[].isSetForCancellation` | boolean |  |
| `results[].membership` | number |  |
| `results[].name` | string |  |
| `results[].object` | string |  |
| `results[].paymentSubscription` | object |  |
| `results[].renewalDate` | object |  |
| `results[].startDate` | string |  |
| `results[].status` | string |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /customer_memberships` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-memberships.md) for the provider-specific parameters and requirements.

