# Simla.com Universal API Examples

These examples use the MindCloud API key and Simla.com connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current API Credentials

Retrieves current API access details from Simla.com.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simlacom/latest/actions/get-current-api-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simlacom/latest/actions/get-current-api-credentials?${params}`, {
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

See the full [Get Current API Credentials action reference](actions/get-current-api-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simlacom/latest/actions/get-current-api-credentials).
