# Climatiq Universal API Examples

These examples use the MindCloud API key and Climatiq connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Data Versions

Retrieves available data versions from Climatiq.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/get-data-versions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/get-data-versions?${params}`, {
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
      "latest": "string",
      "latest_major": 1,
      "latest_minor": 1,
      "latest_release": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Data Versions action reference](actions/get-data-versions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/climatiq/latest/actions/get-data-versions).

## Estimate Emissions

Estimates emissions in Climatiq from activity data.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/estimate-emissions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emissionFactor": {},
  "parameters": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/estimate-emissions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emissionFactor": {},
    "parameters": {}
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "activity_data": {},
      "additional_indicators": {},
      "audit_trail": "string",
      "co2e": 1,
      "co2e_calculation_method": "string",
      "co2e_calculation_origin": "string",
      "co2e_unit": "string",
      "constituent_gases": {},
      "emission_factor": {},
      "notices": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Estimate Emissions action reference](actions/estimate-emissions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/climatiq/latest/actions/estimate-emissions).
