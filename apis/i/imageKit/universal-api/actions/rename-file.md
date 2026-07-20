# ImageKit.io: Rename File

Renames an existing file in ImageKit.io.

```
PUT https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/rename-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageKit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/rename-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/rename-file', {
  method: 'PUT',
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
| `filePath` | string | no | Default: `/default-image-renamed.jpg`. |
| `newFileName` | string | no | Default: `default-image-renamed-2.jpg`. |
| `purgeCache` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ImageKit.io API returns.

## Native endpoint

Through the native ImageKit.io API, this operation is `PUT /files/rename` (base URL `https://api.imagekit.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-file.md) for the provider-specific parameters and requirements.

