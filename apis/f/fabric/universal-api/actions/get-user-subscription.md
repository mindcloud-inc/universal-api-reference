# Fabric: Get User Subscription

Retrieves your subscription from Fabric.

```
GET https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-user-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fabric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-user-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-user-subscription?${params}`, {
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
      "billingCycle": "string",
      "creditOperationCosts": {},
      "creditTopupAt": "string",
      "entitlements": {},
      "hasDefaultPaymentMethod": true,
      "isFreeTrialAvailable": true,
      "planStoreId": "string",
      "planStoreType": "string",
      "status": "string",
      "tier": "string",
      "trialEndingAt": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingCycle` | string |  |
| `creditOperationCosts` | object |  |
| `creditTopupAt` | string |  |
| `entitlements` | object |  |
| `hasDefaultPaymentMethod` | boolean |  |
| `isFreeTrialAvailable` | boolean |  |
| `planStoreId` | string |  |
| `planStoreType` | string |  |
| `status` | string |  |
| `tier` | string |  |
| `trialEndingAt` | string |  |
| `usage` | object |  |

## Native endpoint

Through the native Fabric API, this operation is `GET /v2/subscriptions` (base URL `https://api.fabric.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-subscription.md) for the provider-specific parameters and requirements.

