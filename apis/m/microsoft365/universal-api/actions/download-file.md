# Microsoft 365: Download File

Downloads a file from Microsoft 365.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/download-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/download-file?connectionId=$CONNECTION_ID&itemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/download-file?${params}`, {
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
| `itemId` | string | yes | Drive item ID of the file to download. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft 365 API returns.

## Native endpoint

Through the native Microsoft 365 API, this operation is `GET /v1.0/me/drive/items/:itemId/content` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file.md) for the provider-specific parameters and requirements.

