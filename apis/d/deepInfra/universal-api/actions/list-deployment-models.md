# Deep Infra: List Deployment Models



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-deployment-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-deployment-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-deployment-models?${params}`, {
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
      "description": "string",
      "gpu": "string",
      "is_custom_deployable": true,
      "model_name": "Ava Chen",
      "tags": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Model description. |
| `gpu` | string | GPU class when returned. |
| `is_custom_deployable` | boolean | Whether the model supports custom deployment. |
| `model_name` | string | Deployable model identifier. |
| `tags` | array<string> | Model capability tags. |
| `type` | string | Model task type. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /models/deployment/list` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deployment-models.md) for the provider-specific parameters and requirements.

