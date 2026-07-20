# Ragic: Import From URL

Imports records into Ragic from a URL.

```
POST https://connect.mindcloud.co/v1/universal/ragic/latest/actions/import-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ragic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/import-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tabFolderPath": "string",
  "sheetIndex": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ragic/latest/actions/import-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tabFolderPath": "string",
    "sheetIndex": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tabFolderPath` | string | yes | Folder path segment before the sheet index in the Ragic URL, for example ragic-setup. |
| `sheetIndex` | number | yes | Numeric sheet identifier from the target Ragic resource URL. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ragic API returns.

## Native endpoint

Through the native Ragic API, this operation is `POST /:tabFolderPath/:sheetIndex` (base URL `{{credentials.serverUrl}}/mindcloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-from-url.md) for the provider-specific parameters and requirements.

