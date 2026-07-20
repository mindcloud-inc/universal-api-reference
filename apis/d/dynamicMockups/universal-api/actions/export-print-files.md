# Dynamic Mockups: Export Print Files

Exports print files from a Dynamic Mockups mockup.

```
POST https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/export-print-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynamic Mockups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/export-print-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/export-print-files', {
  method: 'POST',
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



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dynamic Mockups API returns.

## Native endpoint

Through the native Dynamic Mockups API, this operation is `POST api/v1/renders/print-files` (base URL `https://app.dynamicmockups.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-print-files.md) for the provider-specific parameters and requirements.

