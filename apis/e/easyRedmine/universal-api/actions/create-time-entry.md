# Easy Redmine: Create Time Entry

Creates a new time entry in Easy Redmine.

```
POST https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Redmine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timeEntry": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/create-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timeEntry": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeEntry` | object | yes | Time entry payload to create. |

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

Through the native Easy Redmine API, this operation is `POST /time_entries.json` (base URL `https://3f73561b8b.bigus-e5.easy8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-entry.md) for the provider-specific parameters and requirements.

