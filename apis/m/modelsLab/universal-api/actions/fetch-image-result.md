# ModelsLab: Fetch Image Result

Retrieves a generated image result from ModelsLab.

```
GET https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/fetch-image-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ModelsLab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/fetch-image-result?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/fetch-image-result?${params}`, {
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
| `request_id` | string | no | Image generation request ID returned by a generation action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "meta": {},
      "output": [
        "string"
      ],
      "proxy_links": [
        "https://example.com"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `meta` | object |  |
| `output` | array<string> |  |
| `proxy_links` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native ModelsLab API, this operation is `POST /v6/images/fetch/{request_id}` (base URL `https://modelslab.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-image-result.md) for the provider-specific parameters and requirements.

