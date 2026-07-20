# Openlayer: List Projects

Retrieves a list of projects from Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-projects?${params}`, {
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
      "items": [
        {
          "dateCreated": "string",
          "dateUpdated": "string",
          "description": "string",
          "goalCount": 1,
          "id": "string",
          "inferencePipelineCount": 1,
          "links": {
            "app": "https://example.com"
          },
          "name": "Ava Chen",
          "sample": true,
          "taskType": "string",
          "versionCount": 1,
          "workspaceId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].dateCreated` | string |  |
| `items[].dateUpdated` | string |  |
| `items[].description` | string |  |
| `items[].goalCount` | number |  |
| `items[].id` | string |  |
| `items[].inferencePipelineCount` | number |  |
| `items[].links.app` | string |  |
| `items[].name` | string |  |
| `items[].sample` | boolean |  |
| `items[].taskType` | string |  |
| `items[].versionCount` | number |  |
| `items[].workspaceId` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /projects` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

