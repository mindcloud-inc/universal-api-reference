# Deep Infra: List Private Models



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-private-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-private-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-private-models?${params}`, {
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
      "model_name": "Ava Chen",
      "owner": true,
      "public": true,
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
| `description` | string | Private model description. |
| `model_name` | string | Private model identifier. |
| `owner` | boolean | Whether the authenticated account owns the model. |
| `public` | boolean | Whether the model is public. |
| `type` | string | Model task type. |
| `version` | string | Model version identifier. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /models/private/list` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-private-models.md) for the provider-specific parameters and requirements.

