# DiceBear: Generate Avatar Image



```
GET https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/generate-avatar-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DiceBear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/generate-avatar-image?connectionId=$CONNECTION_ID&styleName=Ava%20Chen&format=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "styleName": "Ava Chen",
  "format": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/generate-avatar-image?${params}`, {
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
| `styleName` | string | yes | A current DiceBear 10.x style name in lowercase, using hyphens for multiple words (for example, adventurer-neutral). |
| `format` | list | yes | Output format. JSON metadata is provided by Get Avatar Metadata. One of: `0`, `1`, `2`, `3`, `4`. |
| `seed` | string | no | Seed value used to generate a deterministic avatar. |
| `flip` | list | no | Optional flip: none, horizontal, vertical, or both. One of: `0`, `1`, `2`, `3`. |
| `rotate` | number | no | Optional rotation in degrees from -360 to 360. |
| `scale` | number | no | Optional scale from 0 to 10. |
| `borderRadius` | number | no | Optional border radius from 0 to 50. |
| `backgroundColor` | string | no | Optional hexadecimal background color (for example, b6e3f4). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DiceBear API returns.

## Native endpoint

Through the native DiceBear API, this operation is `GET /:styleName/:format` (base URL `https://api.dicebear.com/10.x`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-avatar-image.md) for the provider-specific parameters and requirements.

