# Carbon Intensity: Get Carbon Intensity Factors

Retrieves carbon intensity factors for fuel types.

```
GET https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-carbon-intensity-factors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbon Intensity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-carbon-intensity-factors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-carbon-intensity-factors?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "Biomass": 1,
          "Coal": 1,
          "Dutch Imports": 1,
          "French Imports": 1,
          "Gas (Combined Cycle)": 1,
          "Gas (Open Cycle)": 1,
          "Hydro": 1,
          "Irish Imports": 1,
          "Nuclear": 1,
          "Oil": 1,
          "Other": 1,
          "Pumped Storage": 1,
          "Solar": 1,
          "Wind": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].Biomass` | number |  |
| `data[].Coal` | number |  |
| `data[].Dutch Imports` | number |  |
| `data[].French Imports` | number |  |
| `data[].Gas (Combined Cycle)` | number |  |
| `data[].Gas (Open Cycle)` | number |  |
| `data[].Hydro` | number |  |
| `data[].Irish Imports` | number |  |
| `data[].Nuclear` | number |  |
| `data[].Oil` | number |  |
| `data[].Other` | number |  |
| `data[].Pumped Storage` | number |  |
| `data[].Solar` | number |  |
| `data[].Wind` | number |  |

## Native endpoint

Through the native Carbon Intensity API, this operation is `GET /intensity/factors` (base URL `https://api.carbonintensity.org.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-carbon-intensity-factors.md) for the provider-specific parameters and requirements.

