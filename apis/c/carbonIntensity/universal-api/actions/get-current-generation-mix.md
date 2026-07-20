# Carbon Intensity: Get Current Generation Mix

Retrieves the current generation mix for Great Britain.

```
GET https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-current-generation-mix
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbon Intensity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-current-generation-mix?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-current-generation-mix?${params}`, {
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
      "data": {
        "from": "string",
        "generationmix": [
          {
            "fuel": "string",
            "perc": 1
          }
        ],
        "to": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.from` | string |  |
| `data.generationmix` | array<object> |  |
| `data.generationmix[].fuel` | string |  |
| `data.generationmix[].perc` | number |  |
| `data.to` | string |  |

## Native endpoint

Through the native Carbon Intensity API, this operation is `GET /generation` (base URL `https://api.carbonintensity.org.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-generation-mix.md) for the provider-specific parameters and requirements.

