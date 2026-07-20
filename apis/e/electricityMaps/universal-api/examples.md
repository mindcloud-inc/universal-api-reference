# Electricity Maps Universal API Examples

These examples use the MindCloud API key and Electricity Maps connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Latest Carbon Intensity



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/get-latest-carbon-intensity?connectionId=$CONNECTION_ID&zone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/get-latest-carbon-intensity?${params}`, {
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
      "_disclaimer": "string",
      "carbonIntensity": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "datetime": "2026-05-07T12:00:00.000Z",
      "emissionFactorType": "string",
      "estimationMethod": "string",
      "isEstimated": true,
      "temporalGranularity": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "zone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Latest Carbon Intensity action reference](actions/get-latest-carbon-intensity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/electricityMaps/latest/actions/get-latest-carbon-intensity).
