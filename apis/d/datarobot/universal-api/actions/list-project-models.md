# Datarobot: List Project Models

Retrieves models for a project from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-project-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-project-models?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-project-models?${params}`, {
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
      "featurelistName": "Ava Chen",
      "id": "string",
      "isFrozen": true,
      "isStarred": true,
      "modelCategory": "string",
      "modelFamily": "string",
      "modelNumber": 1,
      "modelType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `featurelistName` | string |  |
| `id` | string |  |
| `isFrozen` | boolean |  |
| `isStarred` | boolean |  |
| `modelCategory` | string |  |
| `modelFamily` | string |  |
| `modelNumber` | number |  |
| `modelType` | string |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /projects/:projectId/models/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-models.md) for the provider-specific parameters and requirements.

