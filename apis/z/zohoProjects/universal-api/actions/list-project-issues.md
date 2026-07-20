# Zoho Projects: List Project Issues

Retrieves issues from a Zoho Projects project.

```
GET https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-project-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-project-issues?connectionId=$CONNECTION_ID&limit=25&offset=0&portalId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "portalId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-project-issues?${params}`, {
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
| `sortBy` | string | no | Issue sort expression. |
| `viewId` | string | no | Custom view ID. |
| `issueIds` | string | no | Comma-separated issue IDs. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | Raw JSON filter object from Zoho Projects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "issues": [
        [
          {}
        ]
      ],
      "pageInfo": {
        "hasNextPage": true,
        "page": 1,
        "perPage": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `issues[]` | array<object> |  |
| `issues[].addedVia` | string |  |
| `issues[].assignee.email` | string |  |
| `issues[].assignee.firstName` | string |  |
| `issues[].assignee.lastName` | string |  |
| `issues[].assignee.name` | string |  |
| `issues[].assignee.zpuid` | string |  |
| `issues[].assignee.zuid` | number |  |
| `issues[].classification.id` | string |  |
| `issues[].classification.value` | string |  |
| `issues[].createdBy.email` | string |  |
| `issues[].createdBy.firstName` | string |  |
| `issues[].createdBy.lastName` | string |  |
| `issues[].createdBy.name` | string |  |
| `issues[].createdBy.zpuid` | string |  |
| `issues[].createdBy.zuid` | number |  |
| `issues[].createdTime` | date |  |
| `issues[].flag` | string |  |
| `issues[].id` | string |  |
| `issues[].isItReproducible.id` | string |  |
| `issues[].isItReproducible.value` | string |  |
| `issues[].lastUpdatedTime` | date |  |
| `issues[].module.id` | string |  |
| `issues[].module.value` | string |  |
| `issues[].name` | string |  |
| `issues[].prefix` | string |  |
| `issues[].project.id` | string |  |
| `issues[].project.name` | string |  |
| `issues[].severity.id` | string |  |
| `issues[].severity.value` | string |  |
| `issues[].status.color` | string |  |
| `issues[].status.colorHexcode` | string |  |
| `issues[].status.id` | string |  |
| `issues[].status.isClosedType` | boolean |  |
| `issues[].status.name` | string |  |
| `pageInfo.hasNextPage` | boolean |  |
| `pageInfo.page` | number |  |
| `pageInfo.perPage` | number |  |

## Native endpoint

Through the native Zoho Projects API, this operation is `GET /portal/[:PORTALID]/projects/[:PROJECTID]/issues` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-issues.md) for the provider-specific parameters and requirements.

