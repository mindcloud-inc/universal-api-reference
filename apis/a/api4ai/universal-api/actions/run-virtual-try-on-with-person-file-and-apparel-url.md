# api4ai: Run Virtual Try-On with Person File and Apparel URL

Runs virtual try-on from a person file and apparel URL in api4ai.

```
GET https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/run-virtual-try-on-with-person-file-and-apparel-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a api4ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/run-virtual-try-on-with-person-file-and-apparel-url?connectionId=$CONNECTION_ID&image=string&urlApparel=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "image": "string",
  "urlApparel": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/run-virtual-try-on-with-person-file-and-apparel-url?${params}`, {
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
| `image` | file | yes | Person image file to use for the try-on request. |
| `urlApparel` | string | yes | Publicly reachable apparel image URL for the try-on request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "entities": {
          "format": "string",
          "image": "string",
          "kind": "string",
          "name": "Ava Chen",
          "objects": [
            {}
          ],
          "representation": "string"
        },
        "height": 1,
        "md5": "string",
        "name": "Ava Chen",
        "status": {
          "code": "string",
          "message": "string"
        },
        "width": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Transformation results. |
| `results.entities.format` | string | Output image format. |
| `results.entities.image` | string | Output image URL. |
| `results.entities.kind` | string | Output entity kind. |
| `results.entities.name` | string | Output entity name. |
| `results.entities.objects` | array<object> | Detected objects in the output. |
| `results.entities.representation` | string | Output representation type. |
| `results.height` | number | Output image height in pixels. |
| `results.md5` | string | Processed image content hash. |
| `results.name` | string | Processed image name. |
| `results.status.code` | string | Processing status code. |
| `results.status.message` | string | Processing status message. |
| `results.width` | number | Output image width in pixels. |

## Native endpoint

Through the native api4ai API, this operation is `POST /virtual-try-on/v1/results` (base URL `https://api4ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-virtual-try-on-with-person-file-and-apparel-url.md) for the provider-specific parameters and requirements.

