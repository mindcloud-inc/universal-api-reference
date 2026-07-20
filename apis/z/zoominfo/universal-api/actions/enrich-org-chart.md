# Zoominfo: Enrich Org Chart

Enriches an org chart with ZoomInfo data.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-org-chart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-org-chart?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-org-chart?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | no | ZoomInfo unique identifier of the company for which you want to view the org chart |
| `department` | string | no | A comma delimited string of departments to display org charts for. From this endpoint : lookup/department Accepts multiple values in one string, delimited by `,`. |
| `contactAccuracyScoreMin` | string | no | Minimum accuracy score for search results. This score indicates the likelihood that a contact is reachable and still employed by the company listed. Minimum score is 70 and maximum is 99. |
| `contactAccuracyScoreMax` | string | no | Maximum accuracy score for search results. This score indicates the likelihood that a contact is reachable and still employed by the company listed. Minimum score is 70 and maximum is 99. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "id": 1,
        "name": "Ava Chen"
      },
      "department": "string",
      "firstName": "Ava",
      "hasDirectPhone": true,
      "hasEmail": true,
      "id": 1,
      "jobFunction": "string",
      "lastName": "Chen",
      "lastUpdatedDate": "string",
      "middleName": "Ava Chen",
      "orgChartSubTier": 1,
      "orgChartTier": 1,
      "person": {
        "contactAccuracyScore": 1
      },
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.id` | number |  |
| `company.name` | string |  |
| `department` | string |  |
| `firstName` | string |  |
| `hasDirectPhone` | boolean |  |
| `hasEmail` | boolean |  |
| `id` | number |  |
| `jobFunction` | string |  |
| `lastName` | string |  |
| `lastUpdatedDate` | string |  |
| `middleName` | string |  |
| `orgChartSubTier` | number |  |
| `orgChartTier` | number |  |
| `person.contactAccuracyScore` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST enrich/orgchart` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-org-chart.md) for the provider-specific parameters and requirements.

