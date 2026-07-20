# PickFu Universal API Examples

These examples use the MindCloud API key and PickFu connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Surveys



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/list-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/list-surveys?${params}`, {
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
      "completedAt": "2026-05-07T12:00:00.000Z",
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorName": "Ava Chen",
      "elements": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "numResponses": 1,
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "sampleSize": 1,
      "status": "string",
      "targeting": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Surveys action reference](actions/list-surveys.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pickFu/latest/actions/list-surveys).

## Create Project



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "archived": true,
      "bookmarked": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "goal": "string",
      "id": "string",
      "name": "Ava Chen",
      "surveys": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Project action reference](actions/create-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pickFu/latest/actions/create-project).
