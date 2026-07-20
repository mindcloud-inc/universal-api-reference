# ScraperAPI Universal API Examples

These examples use the MindCloud API key and ScraperAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List DataPipeline Projects

Retrieves DataPipeline projects from ScraperAPI.

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

Example response:

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

See the full [List DataPipeline Projects action reference](actions/list-data-pipeline-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scraperAPI/latest/actions/list-data-pipeline-projects).

## Create Amazon Offers DataPipeline Project

Creates an Amazon offers DataPipeline project in ScraperAPI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/create-amazon-offers-data-pipeline-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Amazon Offers Project",
  "projectInput": {},
  "projectInput.list[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/create-amazon-offers-data-pipeline-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Amazon Offers Project",
    "projectInput": {},
    "projectInput.list[]": ["string"]
  })
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Create Amazon Offers DataPipeline Project action reference](actions/create-amazon-offers-data-pipeline-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scraperAPI/latest/actions/create-amazon-offers-data-pipeline-project).
