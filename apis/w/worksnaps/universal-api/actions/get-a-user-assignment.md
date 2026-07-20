# Worksnaps: Get a user assignment

Retrieves a user assignment from a Worksnaps project.

```
GET https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-a-user-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-a-user-assignment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-a-user-assignment?${params}`, {
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
| `project_id` | string | no | ID of the target project |
| `user_assignment_id` | string | no | ID of the user assignment that needs to be fetched |

## Response

```json
{
  "success": true,
  "data": [
    {
      "flag_allow_logging_time": 1,
      "hourly_rate": "https://example.com",
      "id": 1,
      "project_id": 1,
      "role": "string",
      "user_email": "ava@example.com",
      "user_first_name": "Ava",
      "user_id": 1,
      "user_last_name": "Chen",
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
| `hourly_rate` | string | the hourly rate of the user in the project |
| `id` | number | the ID of the user assignment |
| `project_id` | number | the ID of the project |
| `role` | string | the role of the user in the project |
| `user_email` | string | the email of the user |
| `user_first_name` | string | the first name of the user |
| `user_id` | number | the ID of the user |
| `user_last_name` | string | the last name of the user |
| `window_for_adding_offline_time` | number | The number of days after which the user is now allowed to add offline time (-1 means the user is always allowed to delete his/her logged time, 0 means the user is always not allowed to delete his/her logged time. Other allowed values are 1, 2, 3, 5, 7, 10, 14, 30, indicating number of days) |
| `window_for_deleting_time` | number | The number of days after which the user is now allowed to delete logged time (-1 means the user is always allowed to delete his/her logged time, 0 means the user is always not allowed to delete his/her logged time. Other allowed values are 1, 2, 3, 5, 7, 10, 14, 30, indicating number of days) |

## Native endpoint

Through the native Worksnaps API, this operation is `GET /projects/{project_id}/user_assignments/{user_assignment_id}.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-user-assignment.md) for the provider-specific parameters and requirements.

