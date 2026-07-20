# Forecast Universal API Examples

These examples use the MindCloud API key and Forecast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Forecast

Generates forecasts in Forecast.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forecast/latest/actions/generate-forecast?connectionId=$CONNECTION_ID&identifier=SKU-12345&data=%5Bobject%20Object%5D&periods=6&frequency=M&data%5B%5D.date=2024-01-01&data%5B%5D.value=120" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "SKU-12345",
  "data": "[object Object]",
  "periods": "6",
  "frequency": "M",
  "data[].date": "2024-01-01",
  "data[].value": "120"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/forecast/latest/actions/generate-forecast?${params}`, {
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
      "date": "2026-05-07T12:00:00.000Z",
      "forecast": 1,
      "lower": 1,
      "period": 1,
      "upper": 1
    }
  ],
  "meta": {}
}
```

See the full [Generate Forecast action reference](actions/generate-forecast.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/forecast/latest/actions/generate-forecast).
