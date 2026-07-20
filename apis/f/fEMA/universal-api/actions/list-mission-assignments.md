# FEMA: List Mission Assignments

Retrieves mission assignments from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-mission-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-mission-assignments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-mission-assignments?${params}`, {
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
      "actionId": 1,
      "agency": "string",
      "assistanceRequested": "string",
      "dateObligated": "2026-05-07T12:00:00.000Z",
      "dateReceived": "2026-05-07T12:00:00.000Z",
      "declarationTitle": "string",
      "declarationType": "string",
      "disasterNumber": 1,
      "hash": "string",
      "id": "string",
      "incidentId": "string",
      "incidentName": "Ava Chen",
      "incidentType": "string",
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "maAmendNumber": 1,
      "maId": "string",
      "maType": "string",
      "obligationAmount": 1,
      "priority": "string",
      "region": 1,
      "statementOfWork": "string",
      "stt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionId` | number |  |
| `agency` | string |  |
| `assistanceRequested` | string |  |
| `dateObligated` | date |  |
| `dateReceived` | date |  |
| `declarationTitle` | string |  |
| `declarationType` | string |  |
| `disasterNumber` | number |  |
| `hash` | string |  |
| `id` | string |  |
| `incidentId` | string |  |
| `incidentName` | string |  |
| `incidentType` | string |  |
| `lastRefresh` | date |  |
| `maAmendNumber` | number |  |
| `maId` | string |  |
| `maType` | string |  |
| `obligationAmount` | number |  |
| `priority` | string |  |
| `region` | number |  |
| `statementOfWork` | string |  |
| `stt` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v2/MissionAssignments` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-mission-assignments.md) for the provider-specific parameters and requirements.

