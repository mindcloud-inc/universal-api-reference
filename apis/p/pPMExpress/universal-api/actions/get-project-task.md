# PPM Express: Get Project Task



```
GET https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-project-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PPM Express `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-project-task?connectionId=$CONNECTION_ID&projectId=df837bfe-1b68-497c-afe6-3e3ee50eb95e&taskId=03aab579-be16-47ea-8a54-95bbde82fe7d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "df837bfe-1b68-497c-afe6-3e3ee50eb95e",
  "taskId": "03aab579-be16-47ea-8a54-95bbde82fe7d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-project-task?${params}`, {
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
| `projectId` | string | yes | Default: `df837bfe-1b68-497c-afe6-3e3ee50eb95e`. |
| `taskId` | string | yes | Default: `03aab579-be16-47ea-8a54-95bbde82fe7d`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | The requested project task. |

## Native endpoint

Through the native PPM Express API, this operation is `GET /@:tenantName/v1.0/projects/:projectId/tasks/:taskId` (base URL `https://api-us.ppm.express`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-task.md) for the provider-specific parameters and requirements.

