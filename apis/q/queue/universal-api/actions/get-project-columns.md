# Queue: Get Project Columns

Retrieves columns for a Queue project.

```
GET https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-project-columns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-project-columns?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-project-columns?${params}`, {
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
| `projectId` | string | yes | Required path parameter from projects/:project_id/columns. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finished": true,
      "id": "string",
      "position": 1,
      "stage": "string",
      "startTimer": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finished` | boolean |  |
| `id` | string |  |
| `position` | number |  |
| `stage` | string |  |
| `startTimer` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native Queue API, this operation is `GET projects/:project_id/columns` (base URL `https://app.usequeue.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-columns.md) for the provider-specific parameters and requirements.

