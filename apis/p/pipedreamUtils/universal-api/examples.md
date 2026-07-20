# Pipedream Utils Universal API Examples

These examples use the MindCloud API key and Pipedream Utils connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Formatting - [Date/Time] Add/Subtract Time

Adds or subtracts time from a date in Pipedream Utils.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/add-subtract-time?connectionId=$CONNECTION_ID&inputDate=string&operation=string&duration=string&outputFormat=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputDate": "string",
  "operation": "string",
  "duration": "string",
  "outputFormat": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/add-subtract-time?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Formatting - [Date/Time] Add/Subtract Time action reference](actions/add-subtract-time.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipedreamUtils/latest/actions/add-subtract-time).

## Add Files To /tmp

Adds files to /tmp in Pipedream Utils.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/add-files-to-tmp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/add-files-to-tmp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files[]": ["string"]
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
      "": [
        {
          "filename": "Ava Chen",
          "filepath": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Files To /tmp action reference](actions/add-files-to-tmp.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipedreamUtils/latest/actions/add-files-to-tmp).
