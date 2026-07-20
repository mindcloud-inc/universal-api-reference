# Worktivity: List Screenshots

Retrieves screenshots from Worktivity with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-screenshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worktivity `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-screenshots?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-screenshots?${params}`, {
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
      "createDate": "2026-05-07T12:00:00.000Z",
      "data": [
        1
      ],
      "employee": {},
      "filename": "Ava Chen",
      "id": "string",
      "project": {},
      "projectTask": {},
      "type": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createDate` | date |  |
| `data` | array<number> |  |
| `employee` | object |  |
| `filename` | string |  |
| `id` | string |  |
| `project` | object |  |
| `projectTask` | object |  |
| `type` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Worktivity API, this operation is `POST /Screenshots/List` (base URL `https://open-api.useworktivity.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-screenshots.md) for the provider-specific parameters and requirements.

