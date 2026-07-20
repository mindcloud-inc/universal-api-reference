# Stockpilot: Verify API Credentials

Retrieves organization details for the current Stockpilot credentials.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/verify-api-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/verify-api-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/verify-api-credentials?${params}`, {
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
      "features": {
        "accountingConnector": true,
        "apiAccess": true,
        "b2bPortal": true,
        "bestBeforeAlerts": true,
        "createPickingBatch": true,
        "emailCampaign": true,
        "odooConnector": true,
        "productFeed": true,
        "purchaseOrderManagement": true,
        "warehouseManagement": true
      },
      "id": 1,
      "organizationName": "Ava Chen",
      "uniqueId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `features.accountingConnector` | boolean |  |
| `features.apiAccess` | boolean |  |
| `features.b2bPortal` | boolean |  |
| `features.bestBeforeAlerts` | boolean |  |
| `features.createPickingBatch` | boolean |  |
| `features.emailCampaign` | boolean |  |
| `features.odooConnector` | boolean |  |
| `features.productFeed` | boolean |  |
| `features.purchaseOrderManagement` | boolean |  |
| `features.warehouseManagement` | boolean |  |
| `id` | number |  |
| `organizationName` | string |  |
| `uniqueId` | string |  |

## Native endpoint

Through the native Stockpilot API, this operation is `GET /auth/who-is` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-api-credentials.md) for the provider-specific parameters and requirements.

