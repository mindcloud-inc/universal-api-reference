# Twig Business Universal API Examples

These examples use the MindCloud API key and Twig Business connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Lambda Logs



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twigBusiness/latest/actions/get-lambda-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twigBusiness/latest/actions/get-lambda-logs?${params}`, {
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

See the full [Get Lambda Logs action reference](actions/get-lambda-logs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/twigBusiness/latest/actions/get-lambda-logs).
