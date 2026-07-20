# ITM Platform: Get Project Gantt



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-project-gantt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-project-gantt?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-project-gantt?${params}`, {
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
| `projectId` | string | yes | The ITM Platform project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendars": {},
      "dependencies": {},
      "project": {},
      "resources": {},
      "revision": 1,
      "success": true,
      "tasks": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendars` | object |  |
| `dependencies` | object |  |
| `project` | object |  |
| `resources` | object |  |
| `revision` | number |  |
| `success` | boolean |  |
| `tasks` | object |  |
| `type` | string |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /Projects/{ProjectId}/Tasks/Gantt` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-gantt.md) for the provider-specific parameters and requirements.

