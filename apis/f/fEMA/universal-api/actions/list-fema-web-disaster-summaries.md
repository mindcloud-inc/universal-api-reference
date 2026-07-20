# FEMA: List FEMA Web Disaster Summaries

Retrieves FEMA web disaster summaries.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-fema-web-disaster-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-fema-web-disaster-summaries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-fema-web-disaster-summaries?${params}`, {
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
      "disasterNumber": 1,
      "hash": "string",
      "iaLoadDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "paLoadDate": "2026-05-07T12:00:00.000Z",
      "totalAmountHaApproved": 1,
      "totalAmountIhpApproved": 1,
      "totalAmountOnaApproved": 1,
      "totalNumberIaApproved": 1,
      "totalObligatedAmountCatAb": 1,
      "totalObligatedAmountCatC2g": 1,
      "totalObligatedAmountHmgp": 1,
      "totalObligatedAmountPa": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disasterNumber` | number |  |
| `hash` | string |  |
| `iaLoadDate` | date |  |
| `id` | string |  |
| `lastRefresh` | date |  |
| `paLoadDate` | date |  |
| `totalAmountHaApproved` | number |  |
| `totalAmountIhpApproved` | number |  |
| `totalAmountOnaApproved` | number |  |
| `totalNumberIaApproved` | number |  |
| `totalObligatedAmountCatAb` | number |  |
| `totalObligatedAmountCatC2g` | number |  |
| `totalObligatedAmountHmgp` | number |  |
| `totalObligatedAmountPa` | number |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/FemaWebDisasterSummaries` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-fema-web-disaster-summaries.md) for the provider-specific parameters and requirements.

