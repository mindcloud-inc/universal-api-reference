# MetaSurvey Universal API Examples

These examples use the MindCloud API key and MetaSurvey connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Surveys



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-surveys?${params}`, {
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
      "_id": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hasNewData": true,
      "remove_branding": true,
      "showNavigation": true,
      "showProgress": true,
      "title": "string",
      "visibility": true
    }
  ],
  "meta": {}
}
```

See the full [List Surveys action reference](actions/list-surveys.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/metaSurvey/latest/actions/list-surveys).

## Create Folder



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "_id": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "permission": "string",
      "surveysCount": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Folder action reference](actions/create-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/metaSurvey/latest/actions/create-folder).
