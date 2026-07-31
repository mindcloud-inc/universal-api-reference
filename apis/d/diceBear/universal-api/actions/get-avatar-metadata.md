# DiceBear: Get Avatar Metadata



```
GET https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/get-avatar-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DiceBear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/get-avatar-metadata?connectionId=$CONNECTION_ID&styleName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "styleName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/get-avatar-metadata?${params}`, {
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
| `seed` | string | no | Seed used to generate a deterministic avatar. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "options": {},
      "svg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `options` | object | Resolved avatar options and style attributes. |
| `svg` | string | Generated avatar SVG markup. |

## Native endpoint

Through the native DiceBear API, this operation is `GET /:styleName/json` (base URL `https://api.dicebear.com/10.x`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-avatar-metadata.md) for the provider-specific parameters and requirements.

