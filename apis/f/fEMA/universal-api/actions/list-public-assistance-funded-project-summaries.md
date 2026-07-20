# FEMA: List Public Assistance Funded Project Summaries

Retrieves public assistance funded project summaries from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-funded-project-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-funded-project-summaries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-funded-project-summaries?${params}`, {
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
      "applicantName": "Ava Chen",
      "county": "string",
      "declarationDate": "2026-05-07T12:00:00.000Z",
      "disasterNumber": 1,
      "educationApplicant": true,
      "federalObligatedAmount": 1,
      "hash": "string",
      "id": "string",
      "incidentType": "string",
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "numberOfProjects": 1,
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicantName` | string |  |
| `county` | string |  |
| `declarationDate` | date |  |
| `disasterNumber` | number |  |
| `educationApplicant` | boolean |  |
| `federalObligatedAmount` | number |  |
| `hash` | string |  |
| `id` | string |  |
| `incidentType` | string |  |
| `lastRefresh` | date |  |
| `numberOfProjects` | number |  |
| `state` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/PublicAssistanceFundedProjectsSummaries` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-public-assistance-funded-project-summaries.md) for the provider-specific parameters and requirements.

