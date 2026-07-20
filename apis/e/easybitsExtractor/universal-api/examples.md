# easybits Extractor Universal API Examples

These examples use the MindCloud API key and easybits Extractor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Pipeline Connection

Verifies a pipeline connection in easybits Extractor.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easybitsExtractor/latest/actions/verify-pipeline-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easybitsExtractor/latest/actions/verify-pipeline-connection?${params}`, {
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
      "ok": true
    }
  ],
  "meta": {}
}
```

See the full [Verify Pipeline Connection action reference](actions/verify-pipeline-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easybitsExtractor/latest/actions/verify-pipeline-connection).
