# Loopy Loyalty: Create Image Asset



```
POST https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-image-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-image-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "base64String": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-image-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "base64String": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `base64String` | string | yes | Base64 encoded image string. |
| `type` | string | yes | The image type. |
| `opacity` | number | no | The image opacity (0-100). |

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
| `length` | number | Number of image asset identifiers returned. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `POST /imageAsset` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image-asset.md) for the provider-specific parameters and requirements.

