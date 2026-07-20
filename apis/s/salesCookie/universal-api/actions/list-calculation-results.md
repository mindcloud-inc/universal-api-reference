# Sales Cookie: List Calculation Results

Retrieves calculation results from Sales Cookie.

```
GET https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculation-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculation-results?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculation-results?${params}`, {
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
      "adjustedTransactionId": "string",
      "attainedPercentage": 1,
      "attainedValue": 1,
      "attainmentLabel": "string",
      "beneficiaryCurrency": "string",
      "beneficiaryId": "string",
      "beneficiaryValue": 1,
      "calculationId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "createdById": "string",
      "difficulty": "string",
      "explanation": "string",
      "id": "string",
      "isDeleted": true,
      "isEdited": true,
      "isError": true,
      "isEstimated": true,
      "isManual": true,
      "isNonDeductible": true,
      "isRecoverable": true,
      "requiredThreshold": 1,
      "rewardId": "string",
      "rewardType": "string",
      "rewardXml": "string",
      "tag": "string",
      "targetSystemUserId": "string",
      "targetTeamId": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "updatedById": "string",
      "value": 1,
      "weight": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adjustedTransactionId` | string |  |
| `attainedPercentage` | number |  |
| `attainedValue` | number |  |
| `attainmentLabel` | string |  |
| `beneficiaryCurrency` | string |  |
| `beneficiaryId` | string |  |
| `beneficiaryValue` | number |  |
| `calculationId` | string |  |
| `created` | date |  |
| `createdById` | string |  |
| `difficulty` | string |  |
| `explanation` | string |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `isEdited` | boolean |  |
| `isError` | boolean |  |
| `isEstimated` | boolean |  |
| `isManual` | boolean |  |
| `isNonDeductible` | boolean |  |
| `isRecoverable` | boolean |  |
| `requiredThreshold` | number |  |
| `rewardId` | string |  |
| `rewardType` | string |  |
| `rewardXml` | string |  |
| `tag` | string |  |
| `targetSystemUserId` | string |  |
| `targetTeamId` | string |  |
| `updated` | date |  |
| `updatedById` | string |  |
| `value` | number |  |
| `weight` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Sales Cookie API, this operation is `GET /odata/:apiKey/CalculationResult` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calculation-results.md) for the provider-specific parameters and requirements.

