# Bridge Interactive Platform Universal API Examples

These examples use the MindCloud API key and Bridge Interactive Platform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List agents

Retrieves agent records from Bridge Interactive Platform.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/list-agents?connectionId=$CONNECTION_ID&dataset=test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "test"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/list-agents?${params}`, {
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
      "MemberEmail": "ava@example.com",
      "MemberFullName": "Ava Chen",
      "MemberKey": "string",
      "MemberMlsId": "string",
      "MemberStatus": "string",
      "OfficeKey": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List agents action reference](actions/list-agents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bridgeInteractivePlatform/latest/actions/list-agents).
