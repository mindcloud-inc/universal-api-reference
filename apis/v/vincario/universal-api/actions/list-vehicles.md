# Vincario: List Vehicles



```
GET https://connect.mindcloud.co/v1/universal/vincario/latest/actions/list-vehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vincario `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vincario/latest/actions/list-vehicles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vincario/latest/actions/list-vehicles?${params}`, {
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
      "make": "string",
      "makeId": 1,
      "model": "string",
      "modelId": 1,
      "vehicleId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `make` | string |  |
| `makeId` | number |  |
| `model` | string |  |
| `modelId` | number |  |
| `vehicleId` | number |  |

## Native endpoint

Through the native Vincario API, this operation is `GET /:apiKey/:controlSum/decode/value-list/enum/enum_make_model.:format` (base URL `https://api.vincario.com/3.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vehicles.md) for the provider-specific parameters and requirements.

