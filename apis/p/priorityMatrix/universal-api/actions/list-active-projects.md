# Priority Matrix: List Active Projects

Retrieves active projects from Priority Matrix.

```
GET https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/list-active-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/list-active-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/list-active-projects?${params}`, {
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
      "creationDate": 1,
      "idd": 1,
      "name": "Ava Chen",
      "resource_uri": "string",
      "state": 1,
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | number |  |
| `idd` | number |  |
| `name` | string |  |
| `resource_uri` | string |  |
| `state` | number |  |
| `webLink` | string |  |

## Native endpoint

Through the native Priority Matrix API, this operation is `GET /api/v1/project/` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-active-projects.md) for the provider-specific parameters and requirements.

