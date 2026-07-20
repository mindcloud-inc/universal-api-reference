# Datarobot Universal API Examples

These examples use the MindCloud API key and Datarobot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Deployments

Retrieves a list of deployments from Datarobot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-deployments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-deployments?${params}`, {
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
      "approvalStatus": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "hasError": true,
      "id": "string",
      "importance": "string",
      "label": "string",
      "status": "string",
      "userProvidedId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Deployments action reference](actions/list-deployments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datarobot/latest/actions/list-deployments).
