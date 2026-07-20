# FEMA: List Disaster Declarations Summaries

Retrieves disaster declaration summaries from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-disaster-declarations-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-disaster-declarations-summaries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-disaster-declarations-summaries?${params}`, {
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
      "declarationDate": "string",
      "declarationRequestNumber": "string",
      "declarationTitle": "string",
      "declarationType": "string",
      "designatedArea": "string",
      "designatedIncidentTypes": "string",
      "disasterCloseoutDate": {},
      "disasterNumber": 1,
      "femaDeclarationString": "string",
      "fipsCountyCode": "string",
      "fipsStateCode": "string",
      "fyDeclared": 1,
      "hash": "string",
      "hmProgramDeclared": true,
      "iaProgramDeclared": true,
      "id": "string",
      "ihProgramDeclared": true,
      "incidentBeginDate": "string",
      "incidentEndDate": {},
      "incidentId": "string",
      "incidentType": "string",
      "lastIAFilingDate": {},
      "lastRefresh": "string",
      "paProgramDeclared": true,
      "placeCode": "string",
      "region": 1,
      "state": "string",
      "tribalRequest": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `declarationDate` | string |  |
| `declarationRequestNumber` | string |  |
| `declarationTitle` | string |  |
| `declarationType` | string |  |
| `designatedArea` | string |  |
| `designatedIncidentTypes` | string |  |
| `disasterCloseoutDate` | object |  |
| `disasterNumber` | number |  |
| `femaDeclarationString` | string |  |
| `fipsCountyCode` | string |  |
| `fipsStateCode` | string |  |
| `fyDeclared` | number |  |
| `hash` | string |  |
| `hmProgramDeclared` | boolean |  |
| `iaProgramDeclared` | boolean |  |
| `id` | string |  |
| `ihProgramDeclared` | boolean |  |
| `incidentBeginDate` | string |  |
| `incidentEndDate` | object |  |
| `incidentId` | string |  |
| `incidentType` | string |  |
| `lastIAFilingDate` | object |  |
| `lastRefresh` | string |  |
| `paProgramDeclared` | boolean |  |
| `placeCode` | string |  |
| `region` | number |  |
| `state` | string |  |
| `tribalRequest` | boolean |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v2/DisasterDeclarationsSummaries` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-disaster-declarations-summaries.md) for the provider-specific parameters and requirements.

