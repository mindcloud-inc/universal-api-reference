# Scrapeless: Delete Browser Extension

Deletes a browser extension from Scrapeless.

```
DELETE https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/delete-browser-extension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/delete-browser-extension?connectionId=$CONNECTION_ID&extensionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extensionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/delete-browser-extension?${params}`, {
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
| `extensionId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scrapeless API returns.

## Native endpoint

Through the native Scrapeless API, this operation is `DELETE /browser/extensions/:extensionId` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-browser-extension.md) for the provider-specific parameters and requirements.

