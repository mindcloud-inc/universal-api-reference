# BlueSnap: List Subscriptions

Retrieves subscriptions from BlueSnap.

```
GET https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-subscriptions?${params}`, {
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
| `after` | string | no | Return subscriptions after this subscription ID. |
| `before` | string | no | Return subscriptions before this subscription ID. |
| `pagesize` | string | no | Number of results to return. Default: `10`. |
| `status` | string | no | Filter by subscription status. |
| `planId` | string | no | Filter by plan ID. |
| `vaultedShopperId` | string | no | Filter by vaulted shopper ID. |
| `gettotal` | boolean | no | Whether to include total results count. Default: `false`. |
| `fulldescription` | boolean | no | Return full subscription details. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lastPage": true,
      "subscriptions": [
        {
          "currency": "string",
          "nextChargeDate": "string",
          "planId": 1,
          "recurringChargeAmount": 1,
          "status": "string",
          "subscriptionId": 1,
          "vaultedShopperId": 1
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
| `subscriptions[].currency` | string | Currency. |
| `subscriptions[].nextChargeDate` | string | Next charge date. |
| `subscriptions[].planId` | number | Plan ID. |
| `subscriptions[].recurringChargeAmount` | number | Recurring amount. |
| `subscriptions[].status` | string | Subscription status. |
| `subscriptions[].subscriptionId` | number | Subscription ID. |
| `subscriptions[].vaultedShopperId` | number | Vaulted shopper ID. |
| `totalResults` | number | Total results count. |

## Native endpoint

Through the native BlueSnap API, this operation is `GET /recurring/subscriptions` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

