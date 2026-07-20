# Datarobot: Get Registered Model

Retrieves details for a registered model from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-registered-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-registered-model?connectionId=$CONNECTION_ID&registeredModelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "registeredModelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-registered-model?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "isArchived": true,
      "isGlobal": true,
      "lastVersionNum": 1,
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `isGlobal` | boolean |  |
| `lastVersionNum` | number |  |
| `modifiedAt` | date |  |
| `name` | string |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /registeredModels/:registeredModelId/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-registered-model.md) for the provider-specific parameters and requirements.

