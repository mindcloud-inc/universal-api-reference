# Grok: List Models

Retrieves a list of models from Grok.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-models?${params}`, {
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
      "data": [
        {
          "created": 1,
          "id": "string",
          "object": "string",
          "ownedBy": "string"
        }
      ],
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Available xAI models. |
| `data[].created` | number | Unix timestamp when the model entry was created. |
| `data[].id` | string | Model identifier. |
| `data[].object` | string | Provider object type for the model. |
| `data[].ownedBy` | string | Owner of the model. |
| `object` | string | List object type. |

## Native endpoint

Through the native Grok API, this operation is `GET /v1/models` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

