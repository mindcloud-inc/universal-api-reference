# Remote Retrieval Universal API Examples

These examples use the MindCloud API key and Remote Retrieval connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate User

Validates a user in Remote Retrieval.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remoteRetrieval/latest/actions/validate-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remoteRetrieval/latest/actions/validate-user?${params}`, {
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
      "message": "string",
      "phone": "string",
      "response_code": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate User action reference](actions/validate-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/remoteRetrieval/latest/actions/validate-user).
