# FEMA: List Emergency Management Performance Grants

Retrieves emergency management performance grants from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-emergency-management-performance-grants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-emergency-management-performance-grants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-emergency-management-performance-grants?${params}`, {
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
      "fundingAmount": 1,
      "id": "string",
      "legalAgencyName": "Ava Chen",
      "nameOfProgram": "Ava Chen",
      "projectEndDate": "2026-05-07T12:00:00.000Z",
      "projectStartDate": "2026-05-07T12:00:00.000Z",
      "projectType": "string",
      "reportingPeriod": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fundingAmount` | number |  |
| `id` | string |  |
| `legalAgencyName` | string |  |
| `nameOfProgram` | string |  |
| `projectEndDate` | date |  |
| `projectStartDate` | date |  |
| `projectType` | string |  |
| `reportingPeriod` | string |  |
| `state` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v2/EmergencyManagementPerformanceGrants` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-emergency-management-performance-grants.md) for the provider-specific parameters and requirements.

