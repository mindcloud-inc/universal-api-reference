# KLIPY: Get Sticker Items

Retrieves stickers from KLIPY by ID or slug.

```
GET https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/get-sticker-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KLIPY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/get-sticker-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/get-sticker-items?${params}`, {
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
| `ids` | string | no |  |
| `slugs` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KLIPY API returns.

## Native endpoint

Through the native KLIPY API, this operation is `GET /api/v1/:app_key/stickers/items` (base URL `https://api.klipy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sticker-items.md) for the provider-specific parameters and requirements.

