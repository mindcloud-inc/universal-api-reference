# Cloze: Search Projects

Finds projects in Cloze.

```
GET https://connect.mindcloud.co/v1/universal/cloze/latest/actions/search-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/search-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/search-projects?${params}`, {
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
| `assignee` | string | no | Email of the assignee. |
| `freeformquery` | string | no | Natural language query expression. |
| `pagenumber` | number | no | Page number to retrieve starting from 1. Example: `1`. |
| `segment` | string | no | Project segment selector. |
| `stage` | string | no | Project stage selector. |
| `step` | string | no | Next step unique id selector. |
| `countonly` | boolean | no | Return only the available count. |
| `sort` | string | no | Sort order. One of: `0`, `1`, `10`, `11`, `12`, `13`, `14`, `15`, `16`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `group` | string | no | Group order. One of: `0`, `1`. |
| `assigned` | boolean | no | Whether the project is assigned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availablecount": 1,
      "errorcode": 1,
      "pagenumber": 1,
      "pagesize": 1,
      "projects": [
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
| `availablecount` | number | Total number of matching projects. |
| `errorcode` | number | Error code. 0 means success. |
| `pagenumber` | number | Current page number. |
| `pagesize` | number | Maximum number of results returned per page. |
| `projects[]` | array<object> | Matching projects. |
| `projects[].appLinks[]` | array<object> | External app links associated with the project. |
| `projects[].appLinks[].source` | string | External source domain. |
| `projects[].appLinks[].uniqueid` | string | External unique identifier. |
| `projects[].createdDate` | string | Project creation date. |
| `projects[].direct` | string | Direct identifier for the project. |
| `projects[].firstSeen` | number | UTC milliseconds when the project was first seen. |
| `projects[].lastChanged` | number | UTC milliseconds when the project last changed. |
| `projects[].name` | string | Project name. |
| `projects[].segment` | string | Project segment. |
| `projects[].stage` | string | Project stage. |
| `projects[].step` | string | Project next step. |
| `projects[].summary` | string | Project summary. |
| `projects[].syncKey` | string | Cloze sync key for the project. |
| `projects[].userKey` | string | Owning Cloze user key. |
| `projects[].views[]` | array<string> | Views that include the project. |
| `projects[].visibility` | string | Visibility of the project. |

## Native endpoint

Through the native Cloze API, this operation is `GET /v1/projects/find` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-projects.md) for the provider-specific parameters and requirements.

