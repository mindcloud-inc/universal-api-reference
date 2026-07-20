# ImageKit.io: Get Extension

Retrieves a saved extension from ImageKit.io.

```
GET https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/get-extension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageKit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/get-extension?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/get-extension?${params}`, {
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
| `extensionId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ImageKit.io API returns.

## Native endpoint

Through the native ImageKit.io API, this operation is `GET /saved-extensions/:extensionId` (base URL `https://api.imagekit.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extension.md) for the provider-specific parameters and requirements.

