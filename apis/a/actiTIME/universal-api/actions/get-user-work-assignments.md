# actiTIME: Get User Work Assignments

Retrieves a user's work assignments from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-user-work-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-user-work-assignments?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-user-work-assignments?${params}`, {
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
| `uid` | string | yes | User ID or username. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allScope": true,
      "customerIds": [
        1
      ],
      "projectIds": [
        1
      ],
      "taskIds": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allScope` | boolean | Whether the user is assigned all customers, projects, and tasks. |
| `customerIds` | array<number> | Assigned customer identifiers. |
| `projectIds` | array<number> | Assigned project identifiers. |
| `taskIds` | array<number> | Assigned task identifiers. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /users/:uid/workAssignments` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-work-assignments.md) for the provider-specific parameters and requirements.

