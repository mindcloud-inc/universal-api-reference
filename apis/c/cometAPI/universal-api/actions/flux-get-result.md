# CometAPI: Flux Get Result

Retrieves a Flux image result from CometAPI.

```
GET https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/flux-get-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/flux-get-result?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/flux-get-result?${params}`, {
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
| `id` | string | yes | Flux task identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "result": {},
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
| `result` | object |  |
| `status` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `GET /flux/v1/get_result` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/flux-get-result.md) for the provider-specific parameters and requirements.

