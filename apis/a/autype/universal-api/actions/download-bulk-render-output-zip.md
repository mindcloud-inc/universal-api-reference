# Autype: Download Bulk Render Output ZIP

Downloads a bulk render output ZIP from Autype.

```
GET https://connect.mindcloud.co/v1/universal/autype/latest/actions/download-bulk-render-output-zip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autype `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autype/latest/actions/download-bulk-render-output-zip?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autype/latest/actions/download-bulk-render-output-zip?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Autype API returns.

## Native endpoint

Through the native Autype API, this operation is `GET /bulk-render/{bulkJobId}/download` (base URL `https://api.autype.com/api/v1/dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-bulk-render-output-zip.md) for the provider-specific parameters and requirements.

