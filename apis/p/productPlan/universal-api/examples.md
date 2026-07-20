# ProductPlan Universal API Examples

These examples use the MindCloud API key and ProductPlan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Status

Retrieves application status details from ProductPlan.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-status?${params}`, {
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
      "application": "string",
      "generated_at": "2026-05-07T12:00:00.000Z",
      "status": {},
      "user": {},
      "version": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Status action reference](actions/get-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/productPlan/latest/actions/get-status).
