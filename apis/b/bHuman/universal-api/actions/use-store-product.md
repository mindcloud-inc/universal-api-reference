# BHuman: Use Store Product

Creates a video instance from a store product in BHuman.

```
POST https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/use-store-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BHuman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/use-store-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/use-store-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | no | Optional folder ID. |
| `id` | string | yes | The store product ID to use. |
| `videoInstanceId` | string | no | Optional existing video instance ID. |
| `workspaceId` | string | yes | The target workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "result": {
        "folderId": "string",
        "product": {
          "actorId": "string",
          "category": 1,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "creatorId": "string",
          "description": "string",
          "downloads": 1,
          "greetings": "string",
          "id": "string",
          "imageUrl": "https://example.com",
          "length": 1,
          "name": "Ava Chen",
          "ratings": 1,
          "reviews": 1,
          "tags": [
            1
          ],
          "textToVideo": true,
          "thumbnail": "string",
          "trainingVideo": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "useCase": {},
          "videoUrl": "https://example.com"
        },
        "segments": [
          "string"
        ],
        "videoId": "string",
        "videoInstanceId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `result.folderId` | string |  |
| `result.product.actorId` | string |  |
| `result.product.category` | number |  |
| `result.product.createdAt` | date |  |
| `result.product.creatorId` | string |  |
| `result.product.description` | string |  |
| `result.product.downloads` | number |  |
| `result.product.greetings` | string |  |
| `result.product.id` | string |  |
| `result.product.imageUrl` | string |  |
| `result.product.length` | number |  |
| `result.product.name` | string |  |
| `result.product.ratings` | number |  |
| `result.product.reviews` | number |  |
| `result.product.tags[]` | number |  |
| `result.product.textToVideo` | boolean |  |
| `result.product.thumbnail` | string |  |
| `result.product.trainingVideo` | string |  |
| `result.product.updatedAt` | date |  |
| `result.product.useCase` | object |  |
| `result.product.videoUrl` | string |  |
| `result.segments[]` | string |  |
| `result.videoId` | string |  |
| `result.videoInstanceId` | string |  |

## Native endpoint

Through the native BHuman API, this operation is `POST https://store.bhuman.ai/api/store/product/use` (base URL `https://studio.bhuman.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/use-store-product.md) for the provider-specific parameters and requirements.

