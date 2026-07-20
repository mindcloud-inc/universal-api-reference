# ScraperAPI: List DataPipeline Projects

Retrieves DataPipeline projects from ScraperAPI.

```
GET https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/list-data-pipeline-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScraperAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/list-data-pipeline-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/list-data-pipeline-projects?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "notificationConfig": {},
      "projectInput": {},
      "projectType": "string",
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "schedulingEnabled": true,
      "scrapingInterval": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | number |  |
| `name` | string |  |
| `notificationConfig` | object |  |
| `projectInput` | object |  |
| `projectType` | string |  |
| `scheduledAt` | date |  |
| `schedulingEnabled` | boolean |  |
| `scrapingInterval` | string |  |

## Native endpoint

Through the native ScraperAPI API, this operation is `GET https://datapipeline.scraperapi.com/api/projects` (base URL `https://api.scraperapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-pipeline-projects.md) for the provider-specific parameters and requirements.

