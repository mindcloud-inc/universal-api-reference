# Host.io Universal API Examples

These examples use the MindCloud API key and Host.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Domain Full Details

Retrieves full domain details from Host.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-domain-full-details?connectionId=$CONNECTION_ID&domain=google.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "google.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-domain-full-details?${params}`, {
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

See the full [Get Domain Full Details action reference](actions/get-domain-full-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hostio/latest/actions/get-domain-full-details).
