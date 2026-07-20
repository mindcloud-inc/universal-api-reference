# Weights & Biases Universal API Examples

These examples use the MindCloud API key and Weights & Biases connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Server Info

Retrieves trace server information from Weights & Biases.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-server-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weightsBiases/latest/actions/get-server-info?${params}`, {
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
      "min_required_weave_python_version": "string",
      "trace_server_version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Server Info action reference](actions/get-server-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weightsBiases/latest/actions/get-server-info).
