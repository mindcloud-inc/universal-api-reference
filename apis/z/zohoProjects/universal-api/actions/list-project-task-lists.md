# Zoho Projects: List Project Task Lists

Retrieves task lists from a Zoho Projects project.

```
GET https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-project-task-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-project-task-lists?connectionId=$CONNECTION_ID&portalId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-project-task-lists?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalId` | string | yes | Zoho Projects portal ID. |
| `projectId` | string | yes | Zoho Projects project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageInfo": {
        "hasNextPage": true,
        "page": 1,
        "pageCount": 1,
        "perPage": 1
      },
      "tasklists": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageInfo.hasNextPage` | boolean |  |
| `pageInfo.page` | number |  |
| `pageInfo.pageCount` | number |  |
| `pageInfo.perPage` | number |  |
| `tasklists[]` | array<object> |  |
| `tasklists[].createdBy.email` | string |  |
| `tasklists[].createdBy.firstName` | string |  |
| `tasklists[].createdBy.lastName` | string |  |
| `tasklists[].createdBy.name` | string |  |
| `tasklists[].createdBy.zpuid` | string |  |
| `tasklists[].createdBy.zuid` | number |  |
| `tasklists[].createdTime` | date |  |
| `tasklists[].flag` | string |  |
| `tasklists[].id` | string |  |
| `tasklists[].lastUpdatedTime` | date |  |
| `tasklists[].metaInfo.countInfo.filteredTaskCount` | number |  |
| `tasklists[].metaInfo.hasComments` | boolean |  |
| `tasklists[].metaInfo.isCompleted` | boolean |  |
| `tasklists[].metaInfo.isGeneral` | boolean |  |
| `tasklists[].metaInfo.isNoneMilestoneTasklist` | boolean |  |
| `tasklists[].metaInfo.isRolled` | boolean |  |
| `tasklists[].milestone.id` | string |  |
| `tasklists[].milestone.name` | string |  |
| `tasklists[].name` | string |  |
| `tasklists[].project.id` | string |  |
| `tasklists[].project.name` | string |  |
| `tasklists[].sequence.milestoneSequence` | number |  |
| `tasklists[].sequence.projectSequence` | number |  |
| `tasklists[].status` | string |  |

## Native endpoint

Through the native Zoho Projects API, this operation is `GET /portal/[:PORTALID]/projects/[:PROJECTID]/tasklists` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-task-lists.md) for the provider-specific parameters and requirements.

