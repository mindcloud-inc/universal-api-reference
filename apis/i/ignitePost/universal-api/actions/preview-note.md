# IgnitePost: Preview Note

Retrieves preview image URLs for a note in IgnitePost.

```
GET https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/preview-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgnitePost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/preview-note?connectionId=$CONNECTION_ID&font=string&message=string&image=string&imageInside=string&imageBackside=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "font": "string",
  "message": "string",
  "image": "string",
  "imageInside": "string",
  "imageBackside": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/preview-note?${params}`, {
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
| `font` | string | yes | IgnitePOST font key from the List Fonts action. |
| `message` | string | yes | Handwritten message content, up to 450 characters. |
| `image` | string | yes | Front image key from List Default Images or a public image URL. |
| `imageInside` | string | yes | A stock image key or image URL for the card interior. |
| `imageBackside` | string | yes | A stock image key or image URL for the card back. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backsideImage": "string",
      "front": "string",
      "inside": "string",
      "insideImage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backsideImage` | string | Preview image URL for the back of the card. |
| `front` | string | Preview image URL for the front of the card. |
| `inside` | string | Preview image URL for the inside handwritten message. |
| `insideImage` | string | Preview image URL for the inside image panel. |

## Native endpoint

Through the native IgnitePost API, this operation is `POST /preview` (base URL `https://dashboard.ignitepost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-note.md) for the provider-specific parameters and requirements.

