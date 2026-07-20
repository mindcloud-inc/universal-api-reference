# PlumDocs Universal API Examples

These examples use the MindCloud API key and PlumDocs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User

Retrieves authenticated user details from PlumDocs.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plumDocs/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plumDocs/latest/actions/get-authenticated-user?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/plumDocs/latest/actions/get-authenticated-user).

## Generate Document

Generates a document from a PlumDocs workflow.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plumDocs/latest/actions/generate-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "wf_abc123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plumDocs/latest/actions/generate-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "wf_abc123"
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
      "data": {},
      "document": {},
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate Document action reference](actions/generate-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/plumDocs/latest/actions/generate-document).
