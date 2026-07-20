# Glam AI: Get Filters

Retrieves available filters from Glam AI.

```
GET https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/get-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Glam AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/get-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/get-filters?${params}`, {
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
      "example_image": "string",
      "example_video": "string",
      "filter_id": "string",
      "generation_price": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `example_image` | string | Example image URL or token. |
| `example_video` | string | Example video URL or token. |
| `filter_id` | string | Unique filter identifier. |
| `generation_price` | number | Generation credit cost. |
| `name` | string | Filter name to pass to Create Generation. |

## Native endpoint

Through the native Glam AI API, this operation is `GET /filters` (base URL `https://api.glam.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-filters.md) for the provider-specific parameters and requirements.

