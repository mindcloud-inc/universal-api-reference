# Sales Cookie: List Calculations

Retrieves calculation records from Sales Cookie.

```
GET https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculations?${params}`, {
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
      "actualThresholdsXml": "string",
      "approvalType": "string",
      "autoReleaseCredits": true,
      "autoReleaseRewards": true,
      "autoReplacePrevious": true,
      "autoRun": true,
      "autoRunId": {},
      "autoRunNotAllowed": true,
      "calculationsFinished": "string",
      "calculationsStarted": "string",
      "created": "string",
      "createdById": "string",
      "creditedTargetCount": 1,
      "creditedTransactionCount": 1,
      "creditsReleased": true,
      "creditsReleasedDate": "string",
      "customProperties": {},
      "debugOutput": {},
      "endDate": "string",
      "id": "string",
      "isDeleted": true,
      "isLocked": true,
      "name": "Ava Chen",
      "nonCreditedTargetCount": 1,
      "planId": "string",
      "planName": "Ava Chen",
      "planSnapshotXml": "string",
      "reRunCalculationId": {},
      "reRunPreserveApprovals": true,
      "reRunPreserveManualResults": true,
      "resultsReleased": true,
      "resultsReleasedDate": "string",
      "resultsReleasedMainDate": "string",
      "scannedTransactionCount": 1,
      "simulatedCount": 1,
      "simulationCount": 1,
      "startDate": "string",
      "status": "string",
      "tag": "string",
      "updated": "string",
      "updatedById": "string",
      "workspaceCurrency": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualThresholdsXml` | string |  |
| `approvalType` | string |  |
| `autoReleaseCredits` | boolean |  |
| `autoReleaseRewards` | boolean |  |
| `autoReplacePrevious` | boolean |  |
| `autoRun` | boolean |  |
| `autoRunId` | object |  |
| `autoRunNotAllowed` | boolean |  |
| `calculationsFinished` | string |  |
| `calculationsStarted` | string |  |
| `created` | string |  |
| `createdById` | string |  |
| `creditedTargetCount` | number |  |
| `creditedTransactionCount` | number |  |
| `creditsReleased` | boolean |  |
| `creditsReleasedDate` | string |  |
| `customProperties` | object |  |
| `debugOutput` | object |  |
| `endDate` | string |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `isLocked` | boolean |  |
| `name` | string |  |
| `nonCreditedTargetCount` | number |  |
| `planId` | string |  |
| `planName` | string |  |
| `planSnapshotXml` | string |  |
| `reRunCalculationId` | object |  |
| `reRunPreserveApprovals` | boolean |  |
| `reRunPreserveManualResults` | boolean |  |
| `resultsReleased` | boolean |  |
| `resultsReleasedDate` | string |  |
| `resultsReleasedMainDate` | string |  |
| `scannedTransactionCount` | number |  |
| `simulatedCount` | number |  |
| `simulationCount` | number |  |
| `startDate` | string |  |
| `status` | string |  |
| `tag` | string |  |
| `updated` | string |  |
| `updatedById` | string |  |
| `workspaceCurrency` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Sales Cookie API, this operation is `GET /odata/:apiKey/Calculation?$top=1` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calculations.md) for the provider-specific parameters and requirements.

