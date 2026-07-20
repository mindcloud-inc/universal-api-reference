# Grok: List Video Generation Models

Retrieves a list of video generation models from Grok.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-video-generation-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-video-generation-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-video-generation-models?${params}`, {
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
      "models": [
        {
          "created": 1,
          "id": "string",
          "object": "string",
          "ownedBy": "string"
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
| `models` | array<object> | Available video generation models. |
| `models[].created` | number | Unix timestamp when the model entry was created. |
| `models[].id` | string | Model identifier. |
| `models[].object` | string | Provider object type for the model. |
| `models[].ownedBy` | string | Owner of the model. |

## Native endpoint

Through the native Grok API, this operation is `GET /v1/video-generation-models` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-video-generation-models.md) for the provider-specific parameters and requirements.

