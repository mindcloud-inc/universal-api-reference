# GoTeamup: Create Customer Membership

Creates a new customer membership in GoTeamup.

```
POST https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-customer-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-customer-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer": 1,
  "membership": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-customer-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer": 1,
    "membership": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | number | yes | Customer ID |
| `membership` | number | yes | Membership ID |

## Response

```json
{
  "success": true,
  "data": [
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
      "startDate": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeHold` | object |  |
| `billedPrice` | object |  |
| `cancellationReason` | object |  |
| `customer` | number |  |
| `discountCode` | object |  |
| `discountCodeMakesFreeForever` | boolean |  |
| `expirationDate` | object |  |
| `id` | number |  |
| `isSetForCancellation` | boolean |  |
| `membership` | number |  |
| `name` | string |  |
| `object` | string |  |
| `paymentSubscription` | object |  |
| `startDate` | string |  |
| `status` | string |  |

## Native endpoint

Through the native GoTeamup API, this operation is `POST /customer_memberships` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-membership.md) for the provider-specific parameters and requirements.

