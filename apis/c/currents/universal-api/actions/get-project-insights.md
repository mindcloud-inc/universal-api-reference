# Currents: Get Project Insights



```
GET https://connect.mindcloud.co/v1/universal/currents/latest/actions/get-project-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Currents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currents/latest/actions/get-project-insights?connectionId=$CONNECTION_ID&dateEnd=string&dateStart=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateEnd": "string",
  "dateStart": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currents/latest/actions/get-project-insights?${params}`, {
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
| `dateEnd` | string | yes | End date for filtering the query results |
| `dateStart` | string | yes | Start date for filtering the query results |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "dateEnd": "string",
        "dateStart": "string",
        "orgId": "string",
        "projectId": "string",
        "results": {}
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.dateEnd` | string |  |
| `data.dateStart` | string |  |
| `data.orgId` | string |  |
| `data.projectId` | string |  |
| `data.results` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Currents API, this operation is `GET /projects/:projectId/insights` (base URL `https://api.currents.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-insights.md) for the provider-specific parameters and requirements.

