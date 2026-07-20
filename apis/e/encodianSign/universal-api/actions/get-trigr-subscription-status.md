# Encodian - Sign: Get Trigr Subscription Status



```
GET https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/get-trigr-subscription-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/get-trigr-subscription-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/get-trigr-subscription-status?${params}`, {
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
      "Errors": [
        "string"
      ],
      "expiryDate": "2026-05-07T12:00:00.000Z",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "monthlyActions": 1,
      "OperationId": "string",
      "OperationStatus": "string",
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
| `availableActionsMonth` | number | Number of triggers remaining for the current calendar month. |
| `availableActionsMonthDec` | number | Decimal trigger availability value. |
| `billingInterval` | string | Billing interval. |
| `Errors` | array<string> | Errors returned by Encodian. |
| `expiryDate` | date | Subscription expiry date and time. |
| `HttpStatusCode` | number | HTTP status code. |
| `HttpStatusMessage` | string | HTTP status message. |
| `monthlyActions` | number | Allowed triggers per month. |
| `OperationId` | string | Unique operation identifier. |
| `OperationStatus` | string | Operation status. |
| `subscriptionEnabled` | boolean | Whether the Encodian subscription is enabled. |
| `subscriptionLevel` | string | Current Encodian subscription level. |

## Native endpoint

Through the native Encodian - Sign API, this operation is `GET /api/v1/Trigr/GetTrigrSubscriptionStatus` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trigr-subscription-status.md) for the provider-specific parameters and requirements.

