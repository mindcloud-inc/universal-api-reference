# FEMA: List Public Assistance Grant Award Activities

Retrieves public assistance grant award activities from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-grant-award-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-grant-award-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-grant-award-activities?${params}`, {
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
      "applicantName": "Ava Chen",
      "county": "string",
      "damageCategoryCode": "string",
      "dateObligated": "2026-05-07T12:00:00.000Z",
      "declarationDate": "2026-05-07T12:00:00.000Z",
      "declarationTitle": "string",
      "disasterNumber": 1,
      "disasterType": "string",
      "eligibilityStatus": "string",
      "federalShareObligated": 1,
      "fundingStatus": "string",
      "id": "string",
      "incidentType": "string",
      "paCloseoutStatus": "string",
      "pnpStatus": true,
      "projectTitle": "string",
      "pwNumber": 1,
      "region": 1,
      "sriaDisaster": true,
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
| `applicantId` | string |  |
| `applicantName` | string |  |
| `county` | string |  |
| `damageCategoryCode` | string |  |
| `dateObligated` | date |  |
| `declarationDate` | date |  |
| `declarationTitle` | string |  |
| `disasterNumber` | number |  |
| `disasterType` | string |  |
| `eligibilityStatus` | string |  |
| `federalShareObligated` | number |  |
| `fundingStatus` | string |  |
| `id` | string |  |
| `incidentType` | string |  |
| `paCloseoutStatus` | string |  |
| `pnpStatus` | boolean |  |
| `projectTitle` | string |  |
| `pwNumber` | number |  |
| `region` | number |  |
| `sriaDisaster` | boolean |  |
| `state` | string |  |
| `stateAbbreviation` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v2/PublicAssistanceGrantAwardActivities` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-public-assistance-grant-award-activities.md) for the provider-specific parameters and requirements.

