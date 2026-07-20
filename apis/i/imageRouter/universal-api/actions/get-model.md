# ImageRouter: Get Model



```
GET https://connect.mindcloud.co/v1/universal/imageRouter/latest/actions/get-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageRouter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageRouter/latest/actions/get-model?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imageRouter/latest/actions/get-model?${params}`, {
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
| `modelId` | string | yes | The ImageRouter model ID, such as google/gemini-2.5-flash. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aliases": [
        [
          "string"
        ]
      ],
      "id": "string",
      "inputs": {},
      "output": [
        [
          "string"
        ]
      ],
      "price": {},
      "release_date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aliases[]` | array<string> | Model aliases. |
| `id` | string | Model identifier. |
| `inputs` | object | Supported input capabilities. |
| `output[]` | array<string> | Model output types. |
| `price` | object | Pricing data. |
| `release_date` | date | Release date when available. |

## Native endpoint

Through the native ImageRouter API, this operation is `GET /v2/models/:modelId` (base URL `https://api.imagerouter.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model.md) for the provider-specific parameters and requirements.

