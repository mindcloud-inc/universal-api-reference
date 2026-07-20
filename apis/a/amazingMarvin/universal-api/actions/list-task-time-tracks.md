# Amazing Marvin: List Task Time Tracks

Retrieves task time tracks from Amazing Marvin.

```
GET https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/list-task-time-tracks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazing Marvin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/list-task-time-tracks?connectionId=$CONNECTION_ID&taskIds%5B%5D=task-id-1%2Ctask-id-2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskIds[]": "task-id-1,task-id-2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/list-task-time-tracks?${params}`, {
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
| `taskIds[]` | array<string> | yes | List of up to 100 task IDs. Example: `task-id-1,task-id-2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskId": "string",
      "times": [
        [
          "2026-05-07T12:00:00.000Z"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskId` | string |  |
| `times[]` | array<date> |  |

## Native endpoint

Through the native Amazing Marvin API, this operation is `POST /tracks` (base URL `https://serv.amazingmarvin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-time-tracks.md) for the provider-specific parameters and requirements.

