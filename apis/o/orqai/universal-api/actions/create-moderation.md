# Orq.ai: Create Moderation

Creates a moderation result in Orq.ai.

```
GET https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-moderation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-moderation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-moderation?${params}`, {
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
      "id": "string",
      "model": "string",
      "results": [
        {
          "categories": {
            "harassment": true,
            "hate": true,
            "illicit": true,
            "sexual": true,
            "violence": true
          },
          "flagged": true
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
| `id` | string |  |
| `model` | string |  |
| `results[].categories.harassment` | boolean |  |
| `results[].categories.hate` | boolean |  |
| `results[].categories.illicit` | boolean |  |
| `results[].categories.sexual` | boolean |  |
| `results[].categories.violence` | boolean |  |
| `results[].flagged` | boolean |  |

## Native endpoint

Through the native Orq.ai API, this operation is `POST /v2/router/moderations` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-moderation.md) for the provider-specific parameters and requirements.

