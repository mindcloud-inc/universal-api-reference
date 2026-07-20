# Google Forms: Create Image Item

Creates an image item in Google Forms.

```
PUT https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-image-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-image-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "sourceUri": "string",
  "locationIndex": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-image-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "sourceUri": "string",
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
| `sourceUri` | string | yes | Source URI for the image. |
| `altText` | string | no | Alternative text for accessibility. |
| `alignment` | list | no | How to align the image in the form. One of: `0`, `1`, `2`. |
| `width` | number | no | Image width in pixels. |
| `locationIndex` | number | yes | Where to place the new image item in the form. |

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

Through the native Google Forms API, this operation is `POST /:formId:batchUpdate` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image-item.md) for the provider-specific parameters and requirements.

