# BHuman: List Store Products

Retrieves available store products from BHuman.

```
GET https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-store-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BHuman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-store-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-store-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "result": [
        {
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
          "ratings": {},
          "reviews": 1,
          "tags": [
            1
          ],
          "textToVideo": true,
          "thumbnail": "string",
          "trainingVideo": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "useCase": "string",
          "videoUrl": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `result[].actorId` | string |  |
| `result[].category` | number |  |
| `result[].createdAt` | date |  |
| `result[].creatorId` | string |  |
| `result[].description` | string |  |
| `result[].downloads` | number |  |
| `result[].greetings` | string |  |
| `result[].id` | string |  |
| `result[].imageUrl` | string |  |
| `result[].length` | number |  |
| `result[].name` | string |  |
| `result[].ratings` | object |  |
| `result[].reviews` | number |  |
| `result[].tags[]` | number |  |
| `result[].textToVideo` | boolean |  |
| `result[].thumbnail` | string |  |
| `result[].trainingVideo` | string |  |
| `result[].updatedAt` | date |  |
| `result[].useCase` | string |  |
| `result[].videoUrl` | string |  |

## Native endpoint

Through the native BHuman API, this operation is `GET https://store.bhuman.ai/api/store/product` (base URL `https://studio.bhuman.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-store-products.md) for the provider-specific parameters and requirements.

