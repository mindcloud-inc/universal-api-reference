# Google Cloud Document AI Universal API Examples

These examples use the MindCloud API key and Google Cloud Document AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Processor Types

Finds processor types in Google Cloud Document AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/list-processor-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/list-processor-types?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Processor Types action reference](actions/list-processor-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleCloudDocumentAI/latest/actions/list-processor-types).

## Cancel Location Operation

Cancels an operation in a Google Cloud Document AI location.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/cancel-location-operation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/cancel-location-operation', {
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

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Cancel Location Operation action reference](actions/cancel-location-operation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleCloudDocumentAI/latest/actions/cancel-location-operation).
