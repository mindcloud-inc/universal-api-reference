# Lokalise: List Projects

Retrieves projects from Lokalise.

```
GET https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lokalise `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/list-projects?${params}`, {
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
      "baseLanguageIso": "string",
      "createdAt": "string",
      "createdByEmail": "ava@example.com",
      "description": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "projectType": "string",
      "teamId": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseLanguageIso` | string |  |
| `createdAt` | string |  |
| `createdByEmail` | string |  |
| `description` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `projectType` | string |  |
| `teamId` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Lokalise API, this operation is `GET /projects` (base URL `https://api.lokalise.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

