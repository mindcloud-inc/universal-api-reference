# HTML/CSS to Image app: Delete Images Batch



```
DELETE https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/delete-images-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTML/CSS to Image app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/delete-images-batch?connectionId=$CONNECTION_ID&ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/delete-images-batch?${params}`, {
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
| `ids[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ids": [
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
| `ids[]` | string | Identifiers echoed by the wrapper for each deleted image in the batch. |

## Native endpoint

Through the native HTML/CSS to Image app API, this operation is `DELETE /v1/image/batch` (base URL `https://hcti.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-images-batch.md) for the provider-specific parameters and requirements.

