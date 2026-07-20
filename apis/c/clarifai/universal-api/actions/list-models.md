# Clarifai: List Models

Retrieves models from Clarifai.

```
GET https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-models?connectionId=$CONNECTION_ID&limit=25&offset=0&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-models?${params}`, {
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
| `appId` | string | yes | Clarifai app ID. |
| `search` | string | no | Search term for model ID or name. |
| `modelTypeId` | string | no | Filter by model type ID. |
| `trainedOnly` | boolean | no | Return only trained models. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "billingType": 1,
      "createdAt": "string",
      "deployRestriction": 1,
      "id": "string",
      "modelTypeId": "string",
      "modifiedAt": "string",
      "name": "Ava Chen",
      "userId": "string",
      "visibility": {
        "gettable": 1
      },
      "workflowRecommended": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `billingType` | number |  |
| `createdAt` | string |  |
| `deployRestriction` | number |  |
| `id` | string |  |
| `modelTypeId` | string |  |
| `modifiedAt` | string |  |
| `name` | string |  |
| `userId` | string |  |
| `visibility.gettable` | number |  |
| `workflowRecommended` | boolean |  |

## Native endpoint

Through the native Clarifai API, this operation is `GET /v2/users/me/apps/:appId/models` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

