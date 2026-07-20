# CometAPI: Get Model



```
GET https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/get-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/get-model?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/get-model?${params}`, {
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
| `modelId` | string | yes | Model ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "owned_by": "string",
      "supported_endpoint_types": [
        "string"
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
| `object` | string |  |
| `owned_by` | string |  |
| `supported_endpoint_types` | array<string> |  |

## Native endpoint

Through the native CometAPI API, this operation is `GET /v1/models/:model_id` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model.md) for the provider-specific parameters and requirements.

