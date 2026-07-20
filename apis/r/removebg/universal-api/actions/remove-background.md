# Remove.bg: Remove Background

Creates a background-removed image in Remove.bg.

```
POST https://connect.mindcloud.co/v1/universal/removebg/latest/actions/remove-background
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remove.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/removebg/latest/actions/remove-background" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/removebg/latest/actions/remove-background', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | no | Source image URL. Provide exactly one image source. |
| `size` | list | no | Maximum output image resolution. One of: `auto`, `full`, `preview`. Default: `preview`. |
| `type` | list | no | Detect or set the foreground type. One of: `animal`, `auto`, `car`, `graphic`, `person`, `product`, `transportation`. Default: `auto`. |
| `typeLevel` | list | no | Classification level for the detected foreground type. One of: `1`, `2`, `latest`, `none`. Default: `1`. |
| `format` | list | no | Result image format. One of: `auto`, `jpg`, `png`, `webp`, `zip`. Default: `auto`. |
| `crop` | boolean | no | Crop empty regions from the result. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageFileB64` | string | no | Base64-encoded source image. Provide exactly one image source. |
| `roi` | string | no | Rectangle region where foreground detection is allowed. Default: `0% 0% 100% 100%`. |
| `cropMargin` | string | no | Margin to add around the cropped subject. Default: `0`. |
| `scale` | string | no | Scale the subject relative to the image size. Default: `original`. |
| `position` | string | no | Position the subject within the image canvas. Default: `original`. |
| `channels` | list | no | Return the final image or only the alpha mask. One of: `alpha`, `rgba`. Default: `rgba`. |
| `shadowType` | string | no | Generate shadows based on the detected or selected foreground type. |
| `shadowOpacity` | string | no | Shadow darkness from 0 to 100 or auto. |
| `semitransparency` | boolean | no | Keep semi-transparent regions in the result where supported. Default: `true`. |
| `bgColor` | string | no | Solid background color to add behind the subject. |
| `bgImageUrl` | string | no | Background image URL to place behind the subject. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "foregroundHeight": 1,
      "foregroundLeft": 1,
      "foregroundTop": 1,
      "foregroundWidth": 1,
      "resultB64": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `foregroundHeight` | number |  |
| `foregroundLeft` | number |  |
| `foregroundTop` | number |  |
| `foregroundWidth` | number |  |
| `resultB64` | string |  |

## Native endpoint

Through the native Remove.bg API, this operation is `POST /removebg` (base URL `https://api.remove.bg/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-background.md) for the provider-specific parameters and requirements.

