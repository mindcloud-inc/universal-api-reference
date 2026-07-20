# ProProfs Project: List Projects

Retrieves a list of projects from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-projects?${params}`, {
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
| `clientId` | string | no | Filter projects by client ID. |
| `limit` | string | no | Maximum number of records to return. |
| `offset` | string | no | Start position for fetching records. |
| `order` | string | no | Sort order. Valid values: projectname, duedate, progress, billablehours, latest. |
| `status` | string | no | Filter projects by status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "active": "string",
          "archived": "string",
          "billableHours": "string",
          "clientId": "string",
          "clientName": "Ava Chen",
          "closed": "string",
          "color": "string",
          "currency": "string",
          "dateCreated": "string",
          "dateModified": "string",
          "description": "string",
          "dueDate": "string",
          "estimatedHours": "string",
          "fixedPrice": "string",
          "hourlyRate": "https://example.com",
          "important": "string",
          "notes": "string",
          "notifications": "string",
          "ongoing": "string",
          "price": "string",
          "progress": "string",
          "projectId": "string",
          "projectName": "Ava Chen",
          "projectOrder": "string",
          "public": "string",
          "recurring": "string",
          "startDate": "string",
          "tags": "string",
          "teams": [
            {
              "teamId": "string",
              "teamName": "Ava Chen"
            }
          ],
          "template": "string",
          "trackedSeconds": "string",
          "uri": "string",
          "userId": "string",
          "users": [
            {
              "userId": "string",
              "userName": "Ava Chen"
            }
          ]
        }
      ],
      "paging": {
        "limit": 1,
        "offset": 1,
        "totalRecords": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].active` | string |  |
| `data[].archived` | string |  |
| `data[].billableHours` | string |  |
| `data[].clientId` | string |  |
| `data[].clientName` | string |  |
| `data[].closed` | string |  |
| `data[].color` | string |  |
| `data[].currency` | string |  |
| `data[].dateCreated` | string |  |
| `data[].dateModified` | string |  |
| `data[].description` | string |  |
| `data[].dueDate` | string |  |
| `data[].estimatedHours` | string |  |
| `data[].fixedPrice` | string |  |
| `data[].hourlyRate` | string |  |
| `data[].important` | string |  |
| `data[].notes` | string |  |
| `data[].notifications` | string |  |
| `data[].ongoing` | string |  |
| `data[].price` | string |  |
| `data[].progress` | string |  |
| `data[].projectId` | string |  |
| `data[].projectName` | string |  |
| `data[].projectOrder` | string |  |
| `data[].public` | string |  |
| `data[].recurring` | string |  |
| `data[].startDate` | string |  |
| `data[].tags` | string |  |
| `data[].teams[].teamId` | string |  |
| `data[].teams[].teamName` | string |  |
| `data[].template` | string |  |
| `data[].trackedSeconds` | string |  |
| `data[].uri` | string |  |
| `data[].userId` | string |  |
| `data[].users[].userId` | string |  |
| `data[].users[].userName` | string |  |
| `paging.limit` | number |  |
| `paging.offset` | number |  |
| `paging.totalRecords` | number |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `GET /projects` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

