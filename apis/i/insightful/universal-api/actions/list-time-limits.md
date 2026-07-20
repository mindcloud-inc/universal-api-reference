# Insightful: List Time Limits

Finds time limits in Insightful by project or employee.

```
GET https://connect.mindcloud.co/v1/universal/insightful/latest/actions/list-time-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/list-time-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightful/latest/actions/list-time-limits?${params}`, {
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
| `employeeId` | string | no | Filter by employee ID. |
| `projectId` | string | no | Filter by project ID. |
| `type` | string | no | Filter by duration type: day, week, or month. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "employeeId": "string",
      "id": "string",
      "limit": 1,
      "modelName": "Ava Chen",
      "organizationId": "string",
      "projectId": "string",
      "start": "2026-05-07T12:00:00.000Z",
      "startInMilliseconds": "2026-05-07T12:00:00.000Z",
      "timezone": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `employeeId` | string |  |
| `id` | string |  |
| `limit` | number |  |
| `modelName` | string |  |
| `organizationId` | string |  |
| `projectId` | string |  |
| `start` | date |  |
| `startInMilliseconds` | date |  |
| `timezone` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Insightful API, this operation is `GET /time-limit` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-limits.md) for the provider-specific parameters and requirements.

