# Flotiq: Get Media Image

Retrieves a transformed media image from Flotiq.

```
GET https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-media-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-media-image?connectionId=$CONNECTION_ID&widthHeight=string&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "widthHeight": "string",
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-media-image?${params}`, {
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
| `widthHeight` | string | yes | The image size preset, for example 400x400. |
| `key` | string | yes | The media object key or filename reference. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Flotiq API returns.

## Native endpoint

Through the native Flotiq API, this operation is `GET https://api.flotiq.com/image/{{widthHeight}}/{{key}}` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-image.md) for the provider-specific parameters and requirements.

