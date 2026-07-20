# Galileo: List Projects

Finds projects in Galileo with pagination.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-projects?${params}`, {
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
      "limit": 1,
      "nextStartingToken": 1,
      "paginated": true,
      "projects": [
        {
          "bookmark": true,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdByUser": {},
          "description": "string",
          "id": "string",
          "labels": [
            "string"
          ],
          "logStreams": [
            {
              "id": "string",
              "name": "Ava Chen"
            }
          ],
          "name": "Ava Chen",
          "numExperiments": 1,
          "numLogstreams": 1,
          "permissions": [
            {
              "action": "string",
              "allowed": true,
              "message": "string"
            }
          ],
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "startingToken": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number |  |
| `nextStartingToken` | number |  |
| `paginated` | boolean |  |
| `projects` | array<object> |  |
| `projects[].bookmark` | boolean |  |
| `projects[].createdAt` | date |  |
| `projects[].createdByUser` | object |  |
| `projects[].description` | string |  |
| `projects[].id` | string |  |
| `projects[].labels` | array<string> |  |
| `projects[].logStreams` | array<object> |  |
| `projects[].logStreams[].id` | string |  |
| `projects[].logStreams[].name` | string |  |
| `projects[].name` | string |  |
| `projects[].numExperiments` | number |  |
| `projects[].numLogstreams` | number |  |
| `projects[].permissions` | array<object> |  |
| `projects[].permissions[].action` | string |  |
| `projects[].permissions[].allowed` | boolean |  |
| `projects[].permissions[].message` | string |  |
| `projects[].updatedAt` | date |  |
| `startingToken` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Galileo API, this operation is `POST /v2/projects/paginated` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

