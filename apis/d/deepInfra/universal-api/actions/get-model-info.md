# Deep Infra: Get Model Info



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-model-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-model-info?connectionId=$CONNECTION_ID&modelName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-model-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelName` | string | yes | DeepInfra model identifier from the model URL path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "featured": true,
      "max_output_tokens": 1,
      "max_tokens": 1,
      "mf_name": "Ava Chen",
      "mf_title": "string",
      "model_name": "Ava Chen",
      "owner": true,
      "pricing": {},
      "public": true,
      "reported_type": "string",
      "tags": [
        "string"
      ],
      "type": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Model description. |
| `featured` | boolean | Whether the model is featured. |
| `max_output_tokens` | number | Maximum output tokens when returned. |
| `max_tokens` | number | Maximum model context tokens when returned. |
| `mf_name` | string | Model family slug. |
| `mf_title` | string | Model family title. |
| `model_name` | string | Deep Infra model identifier. |
| `owner` | boolean | Whether the authenticated account owns the model. |
| `pricing` | object | Model pricing metadata. |
| `public` | boolean | Whether the model is public. |
| `reported_type` | string | Provider-reported model type. |
| `tags` | array<string> | Model capability tags. |
| `type` | string | Model task type. |
| `version` | string | Model version hash. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /models/:model_name` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model-info.md) for the provider-specific parameters and requirements.

