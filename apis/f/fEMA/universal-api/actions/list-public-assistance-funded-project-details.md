# FEMA: List Public Assistance Funded Project Details

Retrieves public assistance funded project details from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-funded-project-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-funded-project-details?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-funded-project-details?${params}`, {
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
      "applicantId": "string",
      "applicationTitle": "string",
      "county": "string",
      "damageCategoryCode": "string",
      "damageCategoryDescrip": "string",
      "declarationDate": "2026-05-07T12:00:00.000Z",
      "disasterNumber": 1,
      "federalShareObligated": 1,
      "firstObligationDate": "2026-05-07T12:00:00.000Z",
      "gmProjectId": 1,
      "hash": "string",
      "incidentType": "string",
      "lastObligationDate": "2026-05-07T12:00:00.000Z",
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "projectAmount": 1,
      "projectProcessStep": "string",
      "projectSize": "string",
      "projectStatus": "string",
      "pwNumber": 1,
      "stateAbbreviation": "string",
      "totalObligated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicantId` | string |  |
| `applicationTitle` | string |  |
| `county` | string |  |
| `damageCategoryCode` | string |  |
| `damageCategoryDescrip` | string |  |
| `declarationDate` | date |  |
| `disasterNumber` | number |  |
| `federalShareObligated` | number |  |
| `firstObligationDate` | date |  |
| `gmProjectId` | number |  |
| `hash` | string |  |
| `incidentType` | string |  |
| `lastObligationDate` | date |  |
| `lastRefresh` | date |  |
| `projectAmount` | number |  |
| `projectProcessStep` | string |  |
| `projectSize` | string |  |
| `projectStatus` | string |  |
| `pwNumber` | number |  |
| `stateAbbreviation` | string |  |
| `totalObligated` | number |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v2/PublicAssistanceFundedProjectsDetails` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-public-assistance-funded-project-details.md) for the provider-specific parameters and requirements.

