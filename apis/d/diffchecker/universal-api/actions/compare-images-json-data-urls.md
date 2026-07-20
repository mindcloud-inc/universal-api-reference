# Diffchecker: Compare Images (JSON, Data URLs)

Compares images in Diffchecker and returns a JSON diff from data URLs.

```
GET https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/compare-images-json-data-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffchecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/compare-images-json-data-urls?connectionId=$CONNECTION_ID&leftImage=string&rightImage=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leftImage": "string",
  "rightImage": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/compare-images-json-data-urls?${params}`, {
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
| `leftImage` | string | yes | Left image as a data URL. |
| `rightImage` | string | yes | Right image as a data URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changedHeight": 1,
      "changedWidth": 1,
      "dataUrl": "https://example.com",
      "diffPixels": 1,
      "height": 1,
      "misMatchPercentage": 1,
      "originalHeight": 1,
      "originalWidth": 1,
      "totalPixels": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changedHeight` | number | Right image height after normalization. |
| `changedWidth` | number | Right image width after normalization. |
| `dataUrl` | string | PNG data URL of the diff image. |
| `diffPixels` | number | Number of differing pixels. |
| `height` | number | Rendered diff height. |
| `misMatchPercentage` | number | Percentage of differing pixels. |
| `originalHeight` | number | Original left image height. |
| `originalWidth` | number | Original left image width. |
| `totalPixels` | number | Total number of compared pixels. |
| `width` | number | Rendered diff width. |

## Native endpoint

Through the native Diffchecker API, this operation is `POST /image` (base URL `https://api.diffchecker.com/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-images-json-data-urls.md) for the provider-specific parameters and requirements.

