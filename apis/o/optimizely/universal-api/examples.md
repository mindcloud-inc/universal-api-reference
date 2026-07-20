# Optimizely Universal API Examples

These examples use the MindCloud API key and Optimizely connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves a list of projects from Optimizely.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-projects?${params}`, {
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
      "accountId": 1,
      "confidenceThreshold": 1,
      "created": "string",
      "id": 1,
      "isClassic": true,
      "isFlagsEnabled": true,
      "lastModified": "string",
      "name": "Ava Chen",
      "platform": "string",
      "status": "string",
      "webSnippet": {
        "codeRevision": 1,
        "enableForceVariation": true,
        "excludeDisabledExperiments": true,
        "excludeNames": true,
        "includeJquery": true,
        "ipAnonymization": true,
        "jsFileSize": 1,
        "library": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/optimizely/latest/actions/list-projects).
