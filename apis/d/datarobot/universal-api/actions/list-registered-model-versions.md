# Datarobot: List Registered Model Versions

Retrieves versions for a registered model from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-registered-model-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-registered-model-versions?connectionId=$CONNECTION_ID&registeredModelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "registeredModelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-registered-model-versions?${params}`, {
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
| `registeredModelId` | string | yes | The ID of the registered model. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeDeploymentCount": 1,
      "buildStatus": "string",
      "id": "string",
      "isArchived": true,
      "isDeprecated": true,
      "modelExecutionType": "string",
      "modelId": "string",
      "name": "Ava Chen",
      "registeredModelId": "string",
      "registeredModelVersion": 1,
      "stage": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeDeploymentCount` | number |  |
| `buildStatus` | string |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `isDeprecated` | boolean |  |
| `modelExecutionType` | string |  |
| `modelId` | string |  |
| `name` | string |  |
| `registeredModelId` | string |  |
| `registeredModelVersion` | number |  |
| `stage` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /registeredModels/:registeredModelId/versions/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-registered-model-versions.md) for the provider-specific parameters and requirements.

