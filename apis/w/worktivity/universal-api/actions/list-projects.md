# Worktivity: List Projects

Retrieves projects from Worktivity with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worktivity `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-projects?${params}`, {
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
      "color": "string",
      "createDate": "2026-05-07T12:00:00.000Z",
      "customerId": "string",
      "employees": [
        {}
      ],
      "id": "string",
      "teams": [
        {}
      ],
      "title": "string",
      "totalBudget": 1,
      "updateDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `createDate` | date |  |
| `customerId` | string |  |
| `employees` | array<object> |  |
| `id` | string |  |
| `teams` | array<object> |  |
| `title` | string |  |
| `totalBudget` | number |  |
| `updateDate` | date |  |

## Native endpoint

Through the native Worktivity API, this operation is `POST /Project/List` (base URL `https://open-api.useworktivity.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

