# FEMA: List Declaration Denials

Retrieves declaration denials from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-declaration-denials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-declaration-denials?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-declaration-denials?${params}`, {
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
      "currentRequestStatus": "string",
      "declarationRequestDate": "2026-05-07T12:00:00.000Z",
      "declarationRequestNumber": 1,
      "declarationRequestType": "string",
      "hmProgramRequested": true,
      "iaProgramRequested": true,
      "id": "string",
      "ihProgramRequested": true,
      "incidentBeginDate": "2026-05-07T12:00:00.000Z",
      "incidentId": 1,
      "incidentName": "Ava Chen",
      "paProgramRequested": true,
      "region": 1,
      "requestedIncidentBeginDate": "2026-05-07T12:00:00.000Z",
      "requestedIncidentEndDate": "2026-05-07T12:00:00.000Z",
      "requestedIncidentTypes": "string",
      "requestStatusDate": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "stateAbbreviation": "string",
      "tribalRequest": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentRequestStatus` | string |  |
| `declarationRequestDate` | date |  |
| `declarationRequestNumber` | number |  |
| `declarationRequestType` | string |  |
| `hmProgramRequested` | boolean |  |
| `iaProgramRequested` | boolean |  |
| `id` | string |  |
| `ihProgramRequested` | boolean |  |
| `incidentBeginDate` | date |  |
| `incidentId` | number |  |
| `incidentName` | string |  |
| `paProgramRequested` | boolean |  |
| `region` | number |  |
| `requestedIncidentBeginDate` | date |  |
| `requestedIncidentEndDate` | date |  |
| `requestedIncidentTypes` | string |  |
| `requestStatusDate` | date |  |
| `state` | string |  |
| `stateAbbreviation` | string |  |
| `tribalRequest` | boolean |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/DeclarationDenials` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-declaration-denials.md) for the provider-specific parameters and requirements.

