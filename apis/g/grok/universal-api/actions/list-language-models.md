# Grok: List Language Models

Retrieves a list of language models from Grok.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-language-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-language-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-language-models?${params}`, {
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
| `models` | array<object> | Available language models. |
| `models[].created` | number | Unix timestamp when the model entry was created. |
| `models[].id` | string | Model identifier. |
| `models[].object` | string | Provider object type for the model. |
| `models[].ownedBy` | string | Owner of the model. |

## Native endpoint

Through the native Grok API, this operation is `GET /v1/language-models` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-language-models.md) for the provider-specific parameters and requirements.

