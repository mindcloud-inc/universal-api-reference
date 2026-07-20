# CometAPI: Replicate Get Prediction

Retrieves a Replicate prediction from CometAPI.

```
GET https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/replicate-get-prediction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/replicate-get-prediction?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/replicate-get-prediction?${params}`, {
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
| `id` | string | yes | Prediction identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "output": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `output` | object |  |
| `status` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `GET /replicate/v1/predictions/:id` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replicate-get-prediction.md) for the provider-specific parameters and requirements.

