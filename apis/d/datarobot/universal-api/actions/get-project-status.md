# Datarobot: Get Project Status

Retrieves the status of a project from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-project-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-project-status?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-project-status?${params}`, {
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
      "autopilotDone": true,
      "stage": "string",
      "stageDescription": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autopilotDone` | boolean |  |
| `stage` | string |  |
| `stageDescription` | string |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /projects/:projectId/status/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-status.md) for the provider-specific parameters and requirements.

