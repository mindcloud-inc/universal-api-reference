# DynaPictures: Delete Generated Image

Deletes a generated image from DynaPictures.

```
DELETE https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/delete-generated-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynaPictures `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/delete-generated-image?connectionId=$CONNECTION_ID&imagePath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imagePath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/delete-generated-image?${params}`, {
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
| `imagePath` | string | yes | Subpath of the generated image returned by DynaPictures. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DynaPictures API returns.

## Native endpoint

Through the native DynaPictures API, this operation is `DELETE /images/:imagePath` (base URL `https://api.dynapictures.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-generated-image.md) for the provider-specific parameters and requirements.

