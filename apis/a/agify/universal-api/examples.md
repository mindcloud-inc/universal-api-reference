# Agify Universal API Examples

These examples use the MindCloud API key and Agify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Predict Age



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agify/latest/actions/predict-age?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agify/latest/actions/predict-age?${params}`, {
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

See the full [Predict Age action reference](actions/predict-age.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agify/latest/actions/predict-age).
