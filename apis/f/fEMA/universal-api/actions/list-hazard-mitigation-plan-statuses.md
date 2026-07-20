# FEMA: List Hazard Mitigation Plan Statuses

Retrieves hazard mitigation plan statuses from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hazard-mitigation-plan-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hazard-mitigation-plan-statuses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hazard-mitigation-plan-statuses?${params}`, {
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
      "apaDate": "2026-05-07T12:00:00.000Z",
      "communityIdNumber": "string",
      "countyName": "Ava Chen",
      "femaRegion": 1,
      "id": "string",
      "jurisdictionType": "string",
      "placeName": "Ava Chen",
      "planApprovalDate": "2026-05-07T12:00:00.000Z",
      "planExpirationDate": "2026-05-07T12:00:00.000Z",
      "planStatus": "string",
      "planTitle": "string",
      "planType": "string",
      "population": 1,
      "state": "string",
      "stateAbbreviation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apaDate` | date |  |
| `communityIdNumber` | string |  |
| `countyName` | string |  |
| `femaRegion` | number |  |
| `id` | string |  |
| `jurisdictionType` | string |  |
| `placeName` | string |  |
| `planApprovalDate` | date |  |
| `planExpirationDate` | date |  |
| `planStatus` | string |  |
| `planTitle` | string |  |
| `planType` | string |  |
| `population` | number |  |
| `state` | string |  |
| `stateAbbreviation` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/HazardMitigationPlanStatuses` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-hazard-mitigation-plan-statuses.md) for the provider-specific parameters and requirements.

