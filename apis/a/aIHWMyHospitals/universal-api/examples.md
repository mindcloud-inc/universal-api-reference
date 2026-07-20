# AIHW MyHospitals Universal API Examples

These examples use the MindCloud API key and AIHW MyHospitals connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Dataset

Retrieves a dataset from AIHW MyHospitals.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/get-dataset?connectionId=$CONNECTION_ID&datasetId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/get-dataset?${params}`, {
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
      "result": {},
      "version_information": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Dataset action reference](actions/get-dataset.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aIHWMyHospitals/latest/actions/get-dataset).
