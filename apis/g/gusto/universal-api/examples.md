# Gusto Universal API Examples

These examples use the MindCloud API key and Gusto connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Token Info

Retrieves OAuth token information from Gusto.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gusto/latest/actions/get-token-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gusto/latest/actions/get-token-info?${params}`, {
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
      "resource": {
        "type": "string",
        "uuid": "string"
      },
      "resourceOwner": {
        "type": "string",
        "uuid": "string"
      },
      "scope": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Token Info action reference](actions/get-token-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gusto/latest/actions/get-token-info).
