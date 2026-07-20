# TickTick: Get Project With Data

Retrieves a project with its tasks and columns from TickTick.

```
GET https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/get-project-with-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TickTick `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/get-project-with-data?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/get-project-with-data?${params}`, {
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
| `projectId` | list<string> | yes | Project identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": [
        {}
      ],
      "project": {},
      "tasks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columns` | array<object> |  |
| `project` | object |  |
| `tasks` | array<object> |  |

## Native endpoint

Through the native TickTick API, this operation is `GET /open/v1/project/:projectId/data` (base URL `https://api.ticktick.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-with-data.md) for the provider-specific parameters and requirements.

