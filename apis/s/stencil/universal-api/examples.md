# Stencil Universal API Examples

These examples use the MindCloud API key and Stencil connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-account?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentProject": {},
      "currentUsage": 1,
      "email": "ava@example.com",
      "id": "string",
      "limitUsage": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stencil/latest/actions/get-account).

## Create Collection Images



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-collection-images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-collection-images', {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "images": [
        {}
      ],
      "metadata": {},
      "modifications": [
        {}
      ],
      "self": "string",
      "status": "string",
      "templates": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Collection Images action reference](actions/create-collection-images.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stencil/latest/actions/create-collection-images).
