# Bannertize: Retrieve Image

Retrieves a generated image and render status from Bannertize.

```
GET https://connect.mindcloud.co/v1/universal/bannertize/latest/actions/retrieve-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannertize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bannertize/latest/actions/retrieve-image?connectionId=$CONNECTION_ID&image_uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "image_uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bannertize/latest/actions/retrieve-image?${params}`, {
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
| `image_uid` | string | yes | The Bannertize image render UID to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bannertize API returns.

## Native endpoint

Through the native Bannertize API, this operation is `GET image/:image_uid` (base URL `https://api.bannertize.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-image.md) for the provider-specific parameters and requirements.

