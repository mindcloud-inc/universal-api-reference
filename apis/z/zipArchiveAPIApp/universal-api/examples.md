# Zip Archive API app Universal API Examples

These examples use the MindCloud API key and Zip Archive API app connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Extract ZIP Archive

Extracts a ZIP archive in Zip Archive API app.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zipArchiveAPIApp/latest/actions/extract-zip-archive?connectionId=$CONNECTION_ID&file=https%3A%2F%2Fgithub.com%2Fgithubtraining%2Fhellogitworld%2Farchive%2Frefs%2Fheads%2Fmaster.zip" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "https://github.com/githubtraining/hellogitworld/archive/refs/heads/master.zip"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zipArchiveAPIApp/latest/actions/extract-zip-archive?${params}`, {
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
      "response": {
        "data": [
          [
            1
          ]
        ],
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Extract ZIP Archive action reference](actions/extract-zip-archive.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zipArchiveAPIApp/latest/actions/extract-zip-archive).

## Create ZIP Archive

Creates a ZIP archive in Zip Archive API app.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zipArchiveAPIApp/latest/actions/create-zip-archive" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipArchiveAPIApp/latest/actions/create-zip-archive', {
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
      "response": {
        "data": [
          [
            1
          ]
        ],
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create ZIP Archive action reference](actions/create-zip-archive.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zipArchiveAPIApp/latest/actions/create-zip-archive).
