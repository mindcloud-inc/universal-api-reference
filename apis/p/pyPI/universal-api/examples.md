# PyPI Universal API Examples

These examples use the MindCloud API key and PyPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get File Provenance

Retrieves provenance for a PyPI distribution file.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-file-provenance?connectionId=$CONNECTION_ID&project=sampleproject&version=4.0.0&filename=sampleproject-4.0.0.tar.gz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "sampleproject",
  "version": "4.0.0",
  "filename": "sampleproject-4.0.0.tar.gz"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-file-provenance?${params}`, {
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
      "attestation_bundles": [
        {}
      ],
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get File Provenance action reference](actions/get-file-provenance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pyPI/latest/actions/get-file-provenance).
