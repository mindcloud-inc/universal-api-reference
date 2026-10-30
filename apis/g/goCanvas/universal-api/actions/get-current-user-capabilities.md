# GoCanvas: Get Current User Capabilities



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/get-current-user-capabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/get-current-user-capabilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/get-current-user-capabilities?${params}`, {
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
      "allowAdminEdit": true,
      "allowPurchase": true,
      "appStore": true,
      "assignmentsEnabled": true,
      "attachmentSizeLimit": 1,
      "departmentsEnabled": true,
      "dispatchEnabled": true,
      "followUpFormId": "string",
      "followUpsEnabled": true,
      "handoffsBatchSize": 1,
      "hipaaCompliant": true,
      "iconImagesBatchSize": 1,
      "id": 1,
      "imageChunkSizeLimit": 1,
      "liveDataEnabled": true,
      "loginHours": 1,
      "mfaFactors": "string",
      "mfaRequired": true,
      "mobileAnnotationsEnabled": true,
      "mobileBuilderEnabled": true,
      "partialSignUp": true,
      "refDataColumnsBatchSize": 1,
      "refImagesBatchSize": 1,
      "saveToCloudEnabled": true,
      "sendLogId": 1,
      "sendLogs": true,
      "sendLogType": 1,
      "showWorkflowHistory": true,
      "stcBatchSize": 1,
      "trackerSyncInterval": 1,
      "trackingEventsEnabled": true,
      "trackingEventsOdoCapture": true,
      "trial": true,
      "type": "string",
      "videoSizeLimitInSeconds": 1,
      "webSignup": true,
      "workflowEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowAdminEdit` | boolean |  |
| `allowPurchase` | boolean |  |
| `appStore` | boolean |  |
| `assignmentsEnabled` | boolean |  |
| `attachmentSizeLimit` | number |  |
| `departmentsEnabled` | boolean |  |
| `dispatchEnabled` | boolean |  |
| `followUpFormId` | string |  |
| `followUpsEnabled` | boolean |  |
| `handoffsBatchSize` | number |  |
| `hipaaCompliant` | boolean |  |
| `iconImagesBatchSize` | number |  |
| `id` | number |  |
| `imageChunkSizeLimit` | number |  |
| `liveDataEnabled` | boolean |  |
| `loginHours` | number |  |
| `mfaFactors` | string |  |
| `mfaRequired` | boolean |  |
| `mobileAnnotationsEnabled` | boolean |  |
| `mobileBuilderEnabled` | boolean |  |
| `partialSignUp` | boolean |  |
| `refDataColumnsBatchSize` | number |  |
| `refImagesBatchSize` | number |  |
| `saveToCloudEnabled` | boolean |  |
| `sendLogId` | number |  |
| `sendLogs` | boolean |  |
| `sendLogType` | number |  |
| `showWorkflowHistory` | boolean |  |
| `stcBatchSize` | number |  |
| `trackerSyncInterval` | number |  |
| `trackingEventsEnabled` | boolean |  |
| `trackingEventsOdoCapture` | boolean |  |
| `trial` | boolean |  |
| `type` | string |  |
| `videoSizeLimitInSeconds` | number |  |
| `webSignup` | boolean |  |
| `workflowEnabled` | boolean |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /me/capabilities` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-capabilities.md) for the provider-specific parameters and requirements.

