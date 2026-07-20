# ProPublica Nonprofit Explorer Universal API Examples

These examples use the MindCloud API key and ProPublica Nonprofit Explorer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organization

Retrieves an organization from ProPublica Nonprofit Explorer by EIN.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proPublicaNonprofitExplorer/latest/actions/get-organization?connectionId=$CONNECTION_ID&ein=142007220" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ein": "142007220"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proPublicaNonprofitExplorer/latest/actions/get-organization?${params}`, {
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
      "api_version": 1,
      "data_source": "string",
      "filings_with_data": [
        {}
      ],
      "filings_without_data": [
        {}
      ],
      "organization": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Organization action reference](actions/get-organization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/proPublicaNonprofitExplorer/latest/actions/get-organization).
