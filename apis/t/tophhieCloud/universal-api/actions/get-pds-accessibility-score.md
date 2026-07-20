# Tophhie Cloud: Get PDS Accessibility Score



```
GET https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-pds-accessibility-score
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tophhie Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-pds-accessibility-score?connectionId=$CONNECTION_ID&did=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "did": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-pds-accessibility-score?${params}`, {
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
| `did` | string | yes | The decentralized identifier for the PDS repository. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "altCoveragePct": 1,
      "imagePosts": 1,
      "imagesWithAlt": 1,
      "postCoveragePct": 1,
      "postsWithAllImagesAlt": 1,
      "score": 1,
      "totalImages": 1,
      "totalPosts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altCoveragePct` | number | Image alt text coverage percentage. |
| `imagePosts` | number | Posts with images. |
| `imagesWithAlt` | number | Images with alt text. |
| `postCoveragePct` | number | Post coverage percentage. |
| `postsWithAllImagesAlt` | number | Posts where all images have alt text. |
| `score` | number | Accessibility score. |
| `totalImages` | number | Total images analyzed. |
| `totalPosts` | number | Total posts analyzed. |

## Native endpoint

Through the native Tophhie Cloud API, this operation is `GET /pds/accessibilityScore/{did}` (base URL `https://api.tophhie.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pds-accessibility-score.md) for the provider-specific parameters and requirements.

