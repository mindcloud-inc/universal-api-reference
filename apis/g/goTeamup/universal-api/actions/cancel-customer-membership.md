# GoTeamup: Cancel Customer Membership

Cancels an existing customer membership in GoTeamup.

```
PUT https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/cancel-customer-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/cancel-customer-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/cancel-customer-membership', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The TeamUp customer membership ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeHold": {},
      "billedPrice": {},
      "cancellationReason": "string",
      "customer": 1,
      "discountCode": {},
      "discountCodeMakesFreeForever": true,
      "expirationDate": "string",
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeHold` | object |  |
| `billedPrice` | object |  |
| `cancellationReason` | string |  |
| `customer` | number |  |
| `discountCode` | object |  |
| `discountCodeMakesFreeForever` | boolean |  |
| `expirationDate` | string |  |
| `id` | number |  |
| `isSetForCancellation` | boolean |  |
| `membership` | number |  |
| `name` | string |  |
| `object` | string |  |
| `paymentSubscription` | object |  |
| `renewalDate` | object |  |
| `startDate` | string |  |
| `status` | string |  |

## Native endpoint

Through the native GoTeamup API, this operation is `POST /customer_memberships/:id/cancel` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-customer-membership.md) for the provider-specific parameters and requirements.

