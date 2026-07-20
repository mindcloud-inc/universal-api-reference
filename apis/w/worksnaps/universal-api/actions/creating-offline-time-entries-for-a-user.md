# Worksnaps: Creating offline time entries for a user

Creates offline time entries for a user in Worksnaps.

```
POST https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/creating-offline-time-entries-for-a-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/creating-offline-time-entries-for-a-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/creating-offline-time-entries-for-a-user', {
  method: 'POST',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | Raw XML request body for this Worksnaps endpoint. |
| `project_id` | string | no | ID of the target project |
| `user_id` | string | no | ID of the target user |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number | Operation status. |

## Native endpoint

Through the native Worksnaps API, this operation is `POST /projects/{project_id}/users/{user_id}/time_entries.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/creating-offline-time-entries-for-a-user.md) for the provider-specific parameters and requirements.

