# Langfuse: List Models

Retrieves models from Langfuse.

```
GET https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-models?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-models?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "inputPrice": 1,
      "isLangfuseManaged": true,
      "matchPattern": "string",
      "modelName": "Ava Chen",
      "outputPrice": 1,
      "prices": {},
      "pricingTiers": [
        {}
      ],
      "startDate": "2026-05-07T12:00:00.000Z",
      "tokenizerConfig": "string",
      "tokenizerId": "string",
      "totalPrice": 1,
      "unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `inputPrice` | number |  |
| `isLangfuseManaged` | boolean |  |
| `matchPattern` | string |  |
| `modelName` | string |  |
| `outputPrice` | number |  |
| `prices` | object |  |
| `pricingTiers` | array<object> |  |
| `startDate` | date |  |
| `tokenizerConfig` | string |  |
| `tokenizerId` | string |  |
| `totalPrice` | number |  |
| `unit` | string |  |

## Native endpoint

Through the native Langfuse API, this operation is `GET /models` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

