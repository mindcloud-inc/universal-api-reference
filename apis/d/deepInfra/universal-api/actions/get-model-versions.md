# Deep Infra: Get Model Versions



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-model-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-model-versions?connectionId=$CONNECTION_ID&modelName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-model-versions?${params}`, {
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
      "created_at": "string",
      "description": "string",
      "model_name": "Ava Chen",
      "status": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Version creation timestamp when returned. |
| `description` | string | Version description when returned. |
| `model_name` | string | Deep Infra model identifier. |
| `status` | string | Version status when returned. |
| `version` | string | Model version identifier. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /models/:model_name/versions` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model-versions.md) for the provider-specific parameters and requirements.

