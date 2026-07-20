# Transport for London Universal API Examples

These examples use the MindCloud API key and Transport for London connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Journey Modes

Retrieves journey planner modes from Transport for London.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/journey-modes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/journey-modes?${params}`, {
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
      "isFarePaying": true,
      "isScheduledService": true,
      "isTflService": true,
      "modeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Journey Modes action reference](actions/journey-modes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/transportForLondon/latest/actions/journey-modes).
