# Bureau of Economic Analysis Universal API Examples

These examples use the MindCloud API key and Bureau of Economic Analysis connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Dataset List

Retrieves available datasets from the Bureau of Economic Analysis.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bureauOfEconomicAnalysis/latest/actions/get-dataset-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bureauOfEconomicAnalysis/latest/actions/get-dataset-list?${params}`, {
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
      "BEAAPI": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Dataset List action reference](actions/get-dataset-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bureauOfEconomicAnalysis/latest/actions/get-dataset-list).
