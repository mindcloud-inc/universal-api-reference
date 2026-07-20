# FEMA: List HMGP Disaster Summaries

Retrieves HMGP disaster summaries from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hmgp-disaster-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hmgp-disaster-summaries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hmgp-disaster-summaries?${params}`, {
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
      "declarationDate": "2026-05-07T12:00:00.000Z",
      "disasterCloseoutStatus": "string",
      "disasterNumber": 1,
      "disasterType": "string",
      "hmgpCloseoutStatus": "string",
      "id": "string",
      "incidentType": "string",
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "lockedInCeilingAmount": 1,
      "mitigationDollarsAvailable": 1,
      "obligatedTotalAmount": 1,
      "region": 1,
      "state": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `declarationDate` | date |  |
| `disasterCloseoutStatus` | string |  |
| `disasterNumber` | number |  |
| `disasterType` | string |  |
| `hmgpCloseoutStatus` | string |  |
| `id` | string |  |
| `incidentType` | string |  |
| `lastRefresh` | date |  |
| `lockedInCeilingAmount` | number |  |
| `mitigationDollarsAvailable` | number |  |
| `obligatedTotalAmount` | number |  |
| `region` | number |  |
| `state` | string |  |
| `title` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v2/HazardMitigationGrantProgramDisasterSummaries` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-hmgp-disaster-summaries.md) for the provider-specific parameters and requirements.

