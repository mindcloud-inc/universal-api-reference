# BlueSnap: List Plans

Retrieves plans from BlueSnap.

```
GET https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-plans?${params}`, {
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
| `after` | string | no | Return plans after this plan ID. |
| `before` | string | no | Return plans before this plan ID. |
| `pagesize` | string | no | Number of results to return. Default: `10`. |
| `status` | string | no | Filter by plan status. |
| `gettotal` | boolean | no | Whether to include total results count. Default: `false`. |
| `fulldescription` | boolean | no | Return full plan details. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lastPage": true,
      "plans": [
        {
          "chargeFrequency": "string",
          "currency": "string",
          "name": "Ava Chen",
          "planId": 1,
          "recurringChargeAmount": 1,
          "status": "string"
        }
      ],
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastPage` | boolean | Whether this is the last page. |
| `plans[].chargeFrequency` | string | Charge frequency. |
| `plans[].currency` | string | Currency. |
| `plans[].name` | string | Plan name. |
| `plans[].planId` | number | Plan ID. |
| `plans[].recurringChargeAmount` | number | Recurring charge amount. |
| `plans[].status` | string | Plan status. |
| `totalResults` | number | Total results count. |

## Native endpoint

Through the native BlueSnap API, this operation is `GET /recurring/plans` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-plans.md) for the provider-specific parameters and requirements.

