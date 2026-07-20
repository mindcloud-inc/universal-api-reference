# Worksnaps: Create a user assignment (i.e., assign a user to a project)

Creates a user assignment in a Worksnaps project.

```
POST https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/create-a-user-assignment-ie-assign-a-user-to-a-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/create-a-user-assignment-ie-assign-a-user-to-a-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/create-a-user-assignment-ie-assign-a-user-to-a-project', {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "flag_allow_logging_time": 1,
      "hourly_rate": 1,
      "id": 1,
      "project_id": 1,
      "role": "string",
      "user_id": 1,
      "window_for_adding_offline_time": 1,
      "window_for_deleting_time": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flag_allow_logging_time` | number | whether this user is allowed logging time in the project (0 or 1) |
| `hourly_rate` | number | the hourly rate of the user in the project |
| `id` | number | the ID of the user assignment |
| `project_id` | number | the ID of the project |
| `role` | string | the role of the user in the project |
| `user_id` | number | the ID of the user |
| `window_for_adding_offline_time` | number | The number of days after which the user is now allowed to add offline time (-1 means the user is always allowed to delete his/her logged time, 0 means the user is always not allowed to delete his/her logged time. Other allowed values are 1, 2, 3, 5, 7, 10, 14, 30, indicating number of days) |
| `window_for_deleting_time` | number | The number of days after which the user is now allowed to delete logged time (-1 means the user is always allowed to delete his/her logged time, 0 means the user is always not allowed to delete his/her logged time. Other allowed values are 1, 2, 3, 5, 7, 10, 14, 30, indicating number of days) |

## Native endpoint

Through the native Worksnaps API, this operation is `POST /projects/{project_id}/user_assignments.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-user-assignment-ie-assign-a-user-to-a-project.md) for the provider-specific parameters and requirements.

