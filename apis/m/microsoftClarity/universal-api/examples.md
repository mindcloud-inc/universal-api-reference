# Microsoft Clarity Universal API Examples

These examples use the MindCloud API key and Microsoft Clarity connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Project Live Insights

Retrieves project live insights from Microsoft Clarity.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftClarity/latest/actions/get-project-live-insights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftClarity/latest/actions/get-project-live-insights?${params}`, {
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
      "information": [
        {}
      ],
      "metricName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Project Live Insights action reference](actions/get-project-live-insights.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoftClarity/latest/actions/get-project-live-insights).
