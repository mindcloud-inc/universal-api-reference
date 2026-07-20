# Loopy Loyalty: Get Strip Image By Image Configuration



```
GET https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-strip-image-by-image-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-strip-image-by-image-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-strip-image-by-image-configuration?${params}`, {
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
| `width` | number | no | Image width. |
| `height` | number | no | Image height. |
| `padding` | number | no | Padding. |
| `totalStamps` | number | no | Total number of stamps. |
| `stampImage` | string | no | Stamp image template ID. |
| `unstampImage` | string | no | Unstamped image template ID. |
| `imageType` | string | no | Image type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "length": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `length` | number | Payload length of the rendered strip image response. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `GET /images` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-strip-image-by-image-configuration.md) for the provider-specific parameters and requirements.

