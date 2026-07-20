# Muna: Retrieve Predictor

Retrieves a predictor from Muna by tag.

```
GET https://connect.mindcloud.co/v1/universal/muna/latest/actions/retrieve-predictor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Muna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/muna/latest/actions/retrieve-predictor?connectionId=$CONNECTION_ID&tag=my-predictor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tag": "my-predictor"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/muna/latest/actions/retrieve-predictor?${params}`, {
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
| `tag` | string | yes | Predictor tag. Example: `my-predictor`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": "string",
      "card": "string",
      "description": "string",
      "name": "Ava Chen",
      "owner": {
        "created": "string",
        "username": "Ava Chen"
      },
      "signature": {
        "inputs": {
          "description": "string",
          "name": "Ava Chen",
          "optional": true,
          "type": "string"
        },
        "outputs": {
          "name": "Ava Chen",
          "type": "string"
        }
      },
      "status": "string",
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `card` | string |  |
| `description` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `owner.created` | string |  |
| `owner.username` | string |  |
| `signature` | object |  |
| `signature.inputs` | array<object> |  |
| `signature.inputs.description` | string |  |
| `signature.inputs.name` | string |  |
| `signature.inputs.optional` | boolean |  |
| `signature.inputs.type` | string |  |
| `signature.outputs` | array<object> |  |
| `signature.outputs.name` | string |  |
| `signature.outputs.type` | string |  |
| `status` | string |  |
| `tag` | string |  |

## Native endpoint

Through the native Muna API, this operation is `GET /v1/predictors/{tag}` (base URL `https://api.muna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-predictor.md) for the provider-specific parameters and requirements.

