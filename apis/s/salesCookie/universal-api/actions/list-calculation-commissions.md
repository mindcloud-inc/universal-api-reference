# Sales Cookie: List Calculation Commissions

Retrieves calculation commissions from Sales Cookie.

```
GET https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculation-commissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculation-commissions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculation-commissions?${params}`, {
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
      "beneficiaryCurrency": "string",
      "beneficiaryId": "string",
      "beneficiaryValue": 1,
      "bucketWeight": 1,
      "calculationCreditId": "string",
      "calculationId": "string",
      "calculationResultId": "string",
      "commissionRate": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "createdById": "string",
      "explanation": "string",
      "id": "string",
      "isAdjusted": true,
      "isDeleted": true,
      "isEstimated": true,
      "isSplitAbove": "string",
      "splitThreshold": "string",
      "tag": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "updatedById": "string",
      "value": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `beneficiaryCurrency` | string |  |
| `beneficiaryId` | string |  |
| `beneficiaryValue` | number |  |
| `bucketWeight` | number |  |
| `calculationCreditId` | string |  |
| `calculationId` | string |  |
| `calculationResultId` | string |  |
| `commissionRate` | number |  |
| `created` | date |  |
| `createdById` | string |  |
| `explanation` | string |  |
| `id` | string |  |
| `isAdjusted` | boolean |  |
| `isDeleted` | boolean |  |
| `isEstimated` | boolean |  |
| `isSplitAbove` | string |  |
| `splitThreshold` | string |  |
| `tag` | string |  |
| `updated` | date |  |
| `updatedById` | string |  |
| `value` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Sales Cookie API, this operation is `GET /odata/:apiKey/CalculationCommission` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calculation-commissions.md) for the provider-specific parameters and requirements.

