# xAI: Get Model

Retrieves a model from the xAI API.

```
GET https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-model?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-model?${params}`, {
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
| `model_id` | string | no | ID of the model to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "id": "string",
      "object": "string",
      "owned_by": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `id` | string |  |
| `object` | string |  |
| `owned_by` | string |  |

## Native endpoint

Through the native xAI API, this operation is `GET /models/:model_id` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model.md) for the provider-specific parameters and requirements.

