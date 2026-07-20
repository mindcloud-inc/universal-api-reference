# Clarifai: Update Dataset

Updates an existing dataset in Clarifai.

```
PATCH https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PATCH "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-dataset', {
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
      "createdAt": "string",
      "defaultAnnotationFilter": {
        "appId": "string",
        "createdAt": "string",
        "id": "string",
        "modifiedAt": "string",
        "userId": "string"
      },
      "description": "string",
      "id": "string",
      "modifiedAt": "string",
      "userId": "string",
      "visibility": {
        "gettable": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `createdAt` | string |  |
| `defaultAnnotationFilter.appId` | string |  |
| `defaultAnnotationFilter.createdAt` | string |  |
| `defaultAnnotationFilter.id` | string |  |
| `defaultAnnotationFilter.modifiedAt` | string |  |
| `defaultAnnotationFilter.userId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `modifiedAt` | string |  |
| `userId` | string |  |
| `visibility.gettable` | number |  |

## Native endpoint

Through the native Clarifai API, this operation is `PATCH /v2/users/{{credentials.userId}}/apps/{{appId}}/datasets` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dataset.md) for the provider-specific parameters and requirements.

