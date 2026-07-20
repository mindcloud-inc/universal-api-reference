# Imagior Universal API Examples

These examples use the MindCloud API key and Imagior connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Account Details

Retrieves account details from Imagior.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imagior/latest/actions/retrieve-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imagior/latest/actions/retrieve-account-details?${params}`, {
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
      "requestCompletionTime": "string",
      "status": "string",
      "statusCode": 1,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "usage": {}
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Account Details action reference](actions/retrieve-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/imagior/latest/actions/retrieve-account-details).

## Generate Image

Creates an image in Imagior from a template.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/imagior/latest/actions/generate-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imagior/latest/actions/generate-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
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
      "details": {},
      "imageURL": "https://example.com",
      "message": "string",
      "requestCompletionTime": "string",
      "status": "string",
      "statusCode": 1,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "usage": {}
    }
  ],
  "meta": {}
}
```

See the full [Generate Image action reference](actions/generate-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/imagior/latest/actions/generate-image).
