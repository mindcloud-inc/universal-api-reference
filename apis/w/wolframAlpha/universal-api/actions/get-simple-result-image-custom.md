# Wolfram Alpha: Get Simple Result Image Custom

Retrieves a custom simple result image from Wolfram Alpha.

```
GET https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-simple-result-image-custom
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wolfram Alpha `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-simple-result-image-custom?connectionId=$CONNECTION_ID&i=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "i": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-simple-result-image-custom?${params}`, {
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
| `background` | string | no |  |
| `foreground` | string | no |  |
| `i` | string | yes |  |
| `width` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "imageUrl": "https://example.com",
      "query": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | Returned content type. |
| `imageUrl` | string | Image URL for the rendered result when available. |
| `query` | string | Original query text. |

## Native endpoint

Through the native Wolfram Alpha API, this operation is `GET /v1/simple` (base URL `https://api.wolframalpha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-simple-result-image-custom.md) for the provider-specific parameters and requirements.

