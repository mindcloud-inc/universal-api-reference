# Datarobot: Get Project

Retrieves details for a project from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-project?${params}`, {
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
| `projectId` | string | yes | The project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "catalogId": "string",
      "catalogVersionId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "fileName": "Ava Chen",
      "id": "string",
      "metric": "string",
      "projectName": "Ava Chen",
      "stage": "string",
      "target": "string",
      "targetType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `catalogId` | string |  |
| `catalogVersionId` | string |  |
| `created` | date |  |
| `fileName` | string |  |
| `id` | string |  |
| `metric` | string |  |
| `projectName` | string |  |
| `stage` | string |  |
| `target` | string |  |
| `targetType` | string |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /projects/:projectId/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

