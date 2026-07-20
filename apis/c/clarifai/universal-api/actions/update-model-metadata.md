# Clarifai: Update Model Metadata

Updates existing model metadata in Clarifai.

```
PATCH https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-model-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PATCH "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-model-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-model-metadata', {
  method: 'PATCH',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | no | Clarifai app ID. |

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
      "metadata": {
        "owner": "string",
        "stage": "string"
      },
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
| `metadata.owner` | string |  |
| `metadata.stage` | string |  |
| `modelTypeId` | string |  |
| `modifiedAt` | string |  |
| `name` | string |  |
| `userId` | string |  |
| `visibility.gettable` | number |  |
| `workflowRecommended` | boolean |  |

## Native endpoint

Through the native Clarifai API, this operation is `PATCH /v2/users/{{credentials.userId}}/apps/{{appId}}/models` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-model-metadata.md) for the provider-specific parameters and requirements.

