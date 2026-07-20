# Encodian - General: Subscription Flowr And Vertr Status

Retrieves Flowr and Vertr subscription status from Encodian.

```
GET https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/subscription-flowr-and-vertr-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - General `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/subscription-flowr-and-vertr-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/subscription-flowr-and-vertr-status?${params}`, {
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
| `availableActionsMonth` | number |  |
| `availableActionsMonthDec` | number |  |
| `billingInterval` | string |  |
| `Errors` | array<string> |  |
| `expiryDate` | date |  |
| `HttpStatusCode` | number |  |
| `HttpStatusMessage` | string |  |
| `monthlyActions` | number |  |
| `OperationId` | string |  |
| `OperationStatus` | string |  |
| `subscriptionEnabled` | boolean |  |
| `subscriptionLevel` | string |  |

## Native endpoint

Through the native Encodian - General API, this operation is `GET /api/v1/General/GetSubscriptionStatus` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscription-flowr-and-vertr-status.md) for the provider-specific parameters and requirements.

