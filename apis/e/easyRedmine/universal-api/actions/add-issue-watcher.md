# Easy Redmine: Add Issue Watcher

Adds a watcher to an issue in Easy Redmine.

```
PUT https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/add-issue-watcher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Redmine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/add-issue-watcher" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/add-issue-watcher', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the issue to add a watcher to. |
| `userId` | number | yes | ID of the user to add as a watcher. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "success": true,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `success` | boolean |  |
| `userId` | number |  |

## Native endpoint

Through the native Easy Redmine API, this operation is `POST /issues/:id/watchers.json` (base URL `https://3f73561b8b.bigus-e5.easy8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-issue-watcher.md) for the provider-specific parameters and requirements.

