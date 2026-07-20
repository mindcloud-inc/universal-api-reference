# Electricity Maps: Get Past Range Carbon Free Energy



```
GET https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/get-past-range-carbon-free-energy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Electricity Maps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/get-past-range-carbon-free-energy?connectionId=$CONNECTION_ID&zone=string&start=string&end=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zone": "string",
  "start": "string",
  "end": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/get-past-range-carbon-free-energy?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `zone` | string | yes |  |
| `start` | string | yes |  |
| `end` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_disclaimer": "string",
      "data": [
        {}
      ],
      "temporalGranularity": "string",
      "zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_disclaimer` | string |  |
| `data` | array<object> |  |
| `temporalGranularity` | string |  |
| `zone` | string |  |

## Native endpoint

Through the native Electricity Maps API, this operation is `GET /carbon-free-energy/past-range` (base URL `https://api.electricitymaps.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-past-range-carbon-free-energy.md) for the provider-specific parameters and requirements.

