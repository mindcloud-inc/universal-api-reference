# Nucleus One: Get Task Stats

Retrieves task statistics from a Nucleus One project.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-task-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-task-stats?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId&projectId=Enter%20projectId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId",
  "projectId": "Enter projectId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-task-stats?${params}`, {
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
| `organizationId` | string | yes | ID of the organization Example: `Enter organizationId`. |
| `projectId` | string | yes | ID of the project Example: `Enter projectId`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activeOnly` | boolean | no | Include only active tasks Example: `Enter activeOnly`. |
| `completedOnly` | boolean | no | Include only completed tasks Example: `Enter completedOnly`. |
| `deniedOnly` | boolean | no | Include only denied tasks Example: `Enter deniedOnly`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$schema": "string",
      "TotalDurationAsString": "string",
      "TotalDurationInMinutes": 1,
      "TotalInFilter": 1,
      "TotalOnTime": 1,
      "TotalPastDue": 1,
      "TotalUnscheduled": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `TotalDurationAsString` | string |  |
| `TotalDurationInMinutes` | number |  |
| `TotalInFilter` | number |  |
| `TotalOnTime` | number |  |
| `TotalPastDue` | number |  |
| `TotalUnscheduled` | number |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projects/:projectId/taskStats` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-stats.md) for the provider-specific parameters and requirements.

