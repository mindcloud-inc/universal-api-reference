# Optimizely: List Projects

Retrieves a list of projects from Optimizely.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `confidenceThreshold` | number |  |
| `created` | string |  |
| `id` | number |  |
| `isClassic` | boolean |  |
| `isFlagsEnabled` | boolean |  |
| `lastModified` | string |  |
| `name` | string |  |
| `platform` | string |  |
| `status` | string |  |
| `webSnippet.codeRevision` | number |  |
| `webSnippet.enableForceVariation` | boolean |  |
| `webSnippet.excludeDisabledExperiments` | boolean |  |
| `webSnippet.excludeNames` | boolean |  |
| `webSnippet.includeJquery` | boolean |  |
| `webSnippet.ipAnonymization` | boolean |  |
| `webSnippet.jsFileSize` | number |  |
| `webSnippet.library` | string |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /projects` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

