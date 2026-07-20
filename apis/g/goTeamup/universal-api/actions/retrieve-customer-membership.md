# GoTeamup: Retrieve Customer Membership

Retrieves a customer membership from GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-customer-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-customer-membership?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-customer-membership?${params}`, {
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
| `id` | number | yes | The TeamUp customer membership ID |

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
| `renewalDate` | object |  |
| `startDate` | string |  |
| `status` | string |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /customer_memberships/:id` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-customer-membership.md) for the provider-specific parameters and requirements.

