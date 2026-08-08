# XOi Universal API Examples

These examples use the MindCloud API key and XOi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Content



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-content?connectionId=$CONNECTION_ID&contentIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contentIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-content?${params}`, {
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
      "createdAt": "string",
      "id": "string",
      "jobIds": [
        {}
      ],
      "lengthBytes": 1,
      "mediaType": "string",
      "orgID": "string",
      "sha256hex": "string",
      "uploadedAt": "string",
      "uploader": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Content action reference](actions/get-content.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xOi/latest/actions/get-content).

## Authenticate



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/authenticate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xOi/latest/actions/authenticate', {
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
  "data": [],
  "meta": {}
}
```

See the full [Authenticate action reference](actions/authenticate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xOi/latest/actions/authenticate).
