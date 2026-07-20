# Google Forms: Create Video Item

Creates a video item in Google Forms.

```
PUT https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-video-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-video-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "youtubeUri": "string",
  "locationIndex": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-video-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "youtubeUri": "string",
    "locationIndex": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The form identifier. |
| `title` | string | no | Optional item title. |
| `youtubeUri` | string | yes | YouTube URI for the video. |
| `caption` | string | no | Text displayed below the video. |
| `alignment` | list | no | How to align the video in the form. One of: `0`, `1`, `2`. |
| `width` | number | no | Video width in pixels. |
| `locationIndex` | number | yes | Where to place the new video item in the form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "writeControl": {
        "requiredRevisionId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `writeControl.requiredRevisionId` | string |  |

## Native endpoint

Through the native Google Forms API, this operation is `POST /:formId:batchUpdate` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video-item.md) for the provider-specific parameters and requirements.

