# FEMA: List Public Assistance Program Deliveries

Retrieves public assistance program deliveries from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-program-deliveries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-program-deliveries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-program-deliveries?${params}`, {
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
      "applicantIdEmmie": "string",
      "applicantIdGm": 1,
      "applicantName": "Ava Chen",
      "applicantProcessStatus": "string",
      "applicantStatus": "string",
      "applicantType": "string",
      "countyApplicantJurisdiction": "string",
      "currentProjectCost": 1,
      "declarationDate": "2026-05-07T12:00:00.000Z",
      "declarationType": "string",
      "disasterNumber": 1,
      "federalShareObligated": 1,
      "hash": "string",
      "id": "string",
      "incidentType": "string",
      "isPnp": true,
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "region": 1,
      "stateCode": "string",
      "stateName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicantIdEmmie` | string |  |
| `applicantIdGm` | number |  |
| `applicantName` | string |  |
| `applicantProcessStatus` | string |  |
| `applicantStatus` | string |  |
| `applicantType` | string |  |
| `countyApplicantJurisdiction` | string |  |
| `currentProjectCost` | number |  |
| `declarationDate` | date |  |
| `declarationType` | string |  |
| `disasterNumber` | number |  |
| `federalShareObligated` | number |  |
| `hash` | string |  |
| `id` | string |  |
| `incidentType` | string |  |
| `isPnp` | boolean |  |
| `lastRefresh` | date |  |
| `region` | number |  |
| `stateCode` | string |  |
| `stateName` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/PublicAssistanceApplicantsProgramDeliveries` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-public-assistance-program-deliveries.md) for the provider-specific parameters and requirements.

