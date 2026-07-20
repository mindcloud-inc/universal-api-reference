# Insightful: Create Time Limit

Creates a new time limit in Insightful.

```
POST https://connect.mindcloud.co/v1/universal/insightful/latest/actions/create-time-limit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/create-time-limit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "limit": 1,
  "projectId": "string",
  "start": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightful/latest/actions/create-time-limit', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "limit": 1,
    "projectId": "string",
    "start": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `employeeId` | string | no | Optional employee ID. Use * for a default project limit. |
| `limit` | number | yes | The limit in minutes. |
| `projectId` | string | yes | The project ID for the limit. |
| `start` | string | yes | The start date and time in YYYY-MM-DD HH:MM:SS format. |
| `timezone` | string | no | Optional IANA timezone. |
| `type` | string | yes | The duration type: day, week, or month. |

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

Through the native Insightful API, this operation is `POST /time-limit` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-limit.md) for the provider-specific parameters and requirements.

