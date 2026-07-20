# Worktivity: Create or Update Project

Creates or updates a project in Worktivity.

```
PUT https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/create-or-update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worktivity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/create-or-update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/create-or-update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native Worktivity API, this operation is `POST /Project/AddUpdateProject` (base URL `https://open-api.useworktivity.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-project.md) for the provider-specific parameters and requirements.

