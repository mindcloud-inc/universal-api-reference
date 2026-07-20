# Worktivity: List Employees

Retrieves employees from Worktivity with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worktivity `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-employees?${params}`, {
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
      "blocked": true,
      "createDate": "2026-05-07T12:00:00.000Z",
      "employeeCode": "string",
      "id": "string",
      "invitation": {},
      "isActive": true,
      "role": 1,
      "team": {},
      "teamId": "string",
      "updateDate": "2026-05-07T12:00:00.000Z",
      "user": {},
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | boolean |  |
| `createDate` | date |  |
| `employeeCode` | string |  |
| `id` | string |  |
| `invitation` | object |  |
| `isActive` | boolean |  |
| `role` | number |  |
| `team` | object |  |
| `teamId` | string |  |
| `updateDate` | date |  |
| `user` | object |  |
| `userId` | string |  |

## Native endpoint

Through the native Worktivity API, this operation is `POST /Employee/List` (base URL `https://open-api.useworktivity.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

