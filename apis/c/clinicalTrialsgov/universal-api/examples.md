# ClinicalTrials.gov Universal API Examples

These examples use the MindCloud API key and ClinicalTrials.gov connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Version



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-api-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-api-version?${params}`, {
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
      "apiVersion": "string",
      "dataTimestamp": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get API Version action reference](actions/get-api-version.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clinicalTrialsgov/latest/actions/get-api-version).
