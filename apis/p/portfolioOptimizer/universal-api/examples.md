# Portfolio Optimizer Universal API Examples

These examples use the MindCloud API key and Portfolio Optimizer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Asset Correlation Matrix



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/asset-correlation-matrix?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/asset-correlation-matrix?${params}`, {
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

See the full [Asset Correlation Matrix action reference](actions/asset-correlation-matrix.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/portfolioOptimizer/latest/actions/asset-correlation-matrix).
