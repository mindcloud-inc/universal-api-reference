# Carbon Intensity: Get Current Regional Carbon Intensity

Retrieves current carbon intensity for Great Britain regions.

```
GET https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-current-regional-carbon-intensity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbon Intensity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-current-regional-carbon-intensity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-current-regional-carbon-intensity?${params}`, {
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
          "from": "string",
          "regions": [
            {
              "dnoregion": "string",
              "generationmix": [
                {
                  "fuel": "string",
                  "perc": 1
                }
              ],
              "intensity": {
                "actual": 1,
                "forecast": 1,
                "index": "string"
              },
              "regionid": 1,
              "shortname": "Ava Chen"
            }
          ],
          "to": "string"
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
| `data[].from` | string |  |
| `data[].regions` | array<object> |  |
| `data[].regions[].dnoregion` | string |  |
| `data[].regions[].generationmix` | array<object> |  |
| `data[].regions[].generationmix[].fuel` | string |  |
| `data[].regions[].generationmix[].perc` | number |  |
| `data[].regions[].intensity` | object |  |
| `data[].regions[].intensity.actual` | number |  |
| `data[].regions[].intensity.forecast` | number |  |
| `data[].regions[].intensity.index` | string |  |
| `data[].regions[].regionid` | number |  |
| `data[].regions[].shortname` | string |  |
| `data[].to` | string |  |

## Native endpoint

Through the native Carbon Intensity API, this operation is `GET /regional` (base URL `https://api.carbonintensity.org.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-regional-carbon-intensity.md) for the provider-specific parameters and requirements.

