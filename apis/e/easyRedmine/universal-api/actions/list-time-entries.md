# Easy Redmine: List Time Entries

Retrieves time entries from Easy Redmine.

```
GET https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/list-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Redmine `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/list-time-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/list-time-entries?${params}`, {
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
      "comments": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "hours": 1,
      "id": 1,
      "issue": {},
      "project": {},
      "spentOn": "2026-05-07T12:00:00.000Z",
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string |  |
| `createdOn` | date |  |
| `hours` | number |  |
| `id` | number |  |
| `issue` | object |  |
| `project` | object |  |
| `spentOn` | date |  |
| `updatedOn` | date |  |
| `user` | object |  |

## Native endpoint

Through the native Easy Redmine API, this operation is `GET /time_entries.json` (base URL `https://3f73561b8b.bigus-e5.easy8.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-entries.md) for the provider-specific parameters and requirements.

