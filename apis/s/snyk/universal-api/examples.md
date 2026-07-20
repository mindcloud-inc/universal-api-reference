# Snyk Universal API Examples

These examples use the MindCloud API key and Snyk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Access Requests

Retrieves access requests for the current Snyk user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-access-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-access-requests?${params}`, {
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
      "data": [
        {}
      ],
      "jsonapi": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

See the full [List Access Requests action reference](actions/get-access-requests.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/snyk/latest/actions/get-access-requests).
