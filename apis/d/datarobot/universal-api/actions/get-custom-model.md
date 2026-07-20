# Datarobot: Get Custom Model

Retrieves details for a custom model from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-custom-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-custom-model?connectionId=$CONNECTION_ID&customModelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customModelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-custom-model?${params}`, {
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
| `customModelId` | string | yes | The ID of the custom model. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "customModelType": "string",
      "deploymentsCount": 1,
      "description": "string",
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "targetName": "Ava Chen",
      "targetType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `createdBy` | string |  |
| `customModelType` | string |  |
| `deploymentsCount` | number |  |
| `description` | string |  |
| `id` | string |  |
| `language` | string |  |
| `name` | string |  |
| `targetName` | string |  |
| `targetType` | string |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /customModels/:customModelId/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-model.md) for the provider-specific parameters and requirements.

