# Encodian: Get Subscription Status

Retrieves subscription status from Encodian.

```
GET https://connect.mindcloud.co/v1/universal/encodian/latest/actions/get-subscription-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/get-subscription-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/get-subscription-status?${params}`, {
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
      "availableActionsMonth": 1,
      "availableActionsMonthDec": 1,
      "billingInterval": "string",
      "expiryDate": "string",
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "monthlyActions": 1,
      "operationId": {},
      "operationStatus": {},
      "subscriptionEnabled": true,
      "subscriptionLevel": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableActionsMonth` | number |  |
| `availableActionsMonthDec` | number |  |
| `billingInterval` | string |  |
| `expiryDate` | string |  |
| `httpStatusCode` | number |  |
| `httpStatusMessage` | string |  |
| `monthlyActions` | number |  |
| `operationId` | object |  |
| `operationStatus` | object |  |
| `subscriptionEnabled` | boolean |  |
| `subscriptionLevel` | string |  |

## Native endpoint

Through the native Encodian API, this operation is `GET /api/v1/General/GetSubscriptionStatus` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription-status.md) for the provider-specific parameters and requirements.

