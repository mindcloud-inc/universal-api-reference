# ParseHub Universal API Examples

These examples use the MindCloud API key and ParseHub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/list-projects?${params}`, {
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
      "projects": [
        {
          "lastReadyRun": {
            "runToken": "string"
          },
          "lastRun": {
            "runToken": "string"
          },
          "mainSite": "string",
          "mainTemplate": "string",
          "optionsJson": "string",
          "title": "string",
          "token": "string"
        }
      ],
      "totalProjects": 1
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/parseHub/latest/actions/list-projects).

## Cancel Run



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/cancel-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "runToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/cancel-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "runToken": "string"
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
      "dataReady": true,
      "endTime": "string",
      "md5sum": "string",
      "pages": 1,
      "projectToken": "string",
      "runToken": "string",
      "startTemplate": "string",
      "startTime": "string",
      "startUrl": "https://example.com",
      "startValue": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Run action reference](actions/cancel-run.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/parseHub/latest/actions/cancel-run).
