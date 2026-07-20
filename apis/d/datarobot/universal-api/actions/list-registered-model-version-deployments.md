# Datarobot: List Registered Model Version Deployments

Retrieves deployments for a registered model version from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-registered-model-version-deployments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-registered-model-version-deployments?connectionId=$CONNECTION_ID&registeredModelId=string&versionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "registeredModelId": "string",
  "versionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-registered-model-version-deployments?${params}`, {
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
| `registeredModelId` | string | yes |  |
| `versionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentlyDeployed": true,
      "id": "string",
      "isChallenger": true,
      "label": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `currentlyDeployed` | boolean |  |
| `id` | string |  |
| `isChallenger` | boolean |  |
| `label` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /registeredModels/:registeredModelId/versions/:versionId/deployments/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-registered-model-version-deployments.md) for the provider-specific parameters and requirements.

