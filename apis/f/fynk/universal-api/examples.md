# fynk Universal API Examples

These examples use the MindCloud API key and fynk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current API Token Details

Retrieves the current API token details from fynk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fynk/latest/actions/get-current-api-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fynk/latest/actions/get-current-api-token-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Current API Token Details action reference](actions/get-current-api-token-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fynk/latest/actions/get-current-api-token-details).

## Create Document File Storage Upload URL

Creates a document file storage upload URL in fynk.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fynk/latest/actions/create-document-file-storage-upload-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fynk/latest/actions/create-document-file-storage-upload-url', {
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

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Document File Storage Upload URL action reference](actions/create-document-file-storage-upload-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fynk/latest/actions/create-document-file-storage-upload-url).
