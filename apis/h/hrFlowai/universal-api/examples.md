# HrFlow.ai Universal API Examples

These examples use the MindCloud API key and HrFlow.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Credentials

Verifies HrFlow.ai API credentials and retrieves team details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hrFlowai/latest/actions/validate-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hrFlowai/latest/actions/validate-credentials?${params}`, {
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

See the full [Validate Credentials action reference](actions/validate-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hrFlowai/latest/actions/validate-credentials).
