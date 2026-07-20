# Pirsonal Universal API Examples

These examples use the MindCloud API key and Pirsonal connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Templates

Retrieves templates from your Pirsonal account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/list-templates?${params}`, {
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
      "analytics": {},
      "date": "string",
      "description": "string",
      "id": "string",
      "inputMedias": [
        {}
      ],
      "inputScripts": [
        "string"
      ],
      "name": "Ava Chen",
      "outProfiles": [
        "string"
      ],
      "secret": "string",
      "status": "string",
      "template_type": "string",
      "videoInputs": {},
      "videoOutput": {},
      "videosCSV": 1
    }
  ],
  "meta": {}
}
```

See the full [List Templates action reference](actions/list-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pirsonal/latest/actions/list-templates).

## Apply Media Pattern

Applies a pattern to existing media in Pirsonal.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/apply-media-pattern" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaID": "string",
  "patter": "audiolevel",
  "action": "info",
  "parameters": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/apply-media-pattern', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaID": "string",
    "patter": "audiolevel",
    "action": "info",
    "parameters": "[object Object]"
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Apply Media Pattern action reference](actions/apply-media-pattern.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pirsonal/latest/actions/apply-media-pattern).
