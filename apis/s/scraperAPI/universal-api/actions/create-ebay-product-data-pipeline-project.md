# ScraperAPI: Create eBay Product DataPipeline Project

Creates an eBay product DataPipeline project in ScraperAPI.

```
POST https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/create-ebay-product-data-pipeline-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScraperAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/create-ebay-product-data-pipeline-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "eBay Product Project",
  "projectInput": {},
  "projectInput.list[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/create-ebay-product-data-pipeline-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "eBay Product Project",
    "projectInput": {},
    "projectInput.list[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The project name. Example: `eBay Product Project`. |
| `projectInput` | object | yes | The project input object. |
| `projectInput.list[]` | array<string> | yes | The list of inputs for the project. |

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

Through the native ScraperAPI API, this operation is `POST https://datapipeline.scraperapi.com/api/projects` (base URL `https://api.scraperapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ebay-product-data-pipeline-project.md) for the provider-specific parameters and requirements.

