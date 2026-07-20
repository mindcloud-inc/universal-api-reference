# ITM Platform: Get Project Sprint



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-project-sprint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-project-sprint?connectionId=$CONNECTION_ID&projectId=string&sprintId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "sprintId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-project-sprint?${params}`, {
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
| `sprintId` | string | yes | The ITM Platform sprint ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "description": "string",
      "duration": "string",
      "endDate": "string",
      "id": "string",
      "name": "Ava Chen",
      "projectId": 1,
      "startDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `description` | string |  |
| `duration` | string |  |
| `endDate` | string |  |
| `id` | string |  |
| `name` | string |  |
| `projectId` | number |  |
| `startDate` | string |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /v2/Projects/{ProjectId}/Sprints/{SprintId}` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-sprint.md) for the provider-specific parameters and requirements.

