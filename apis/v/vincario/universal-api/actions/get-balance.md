# Vincario: Get Balance



```
GET https://connect.mindcloud.co/v1/universal/vincario/latest/actions/get-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vincario `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vincario/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vincario/latest/actions/get-balance?${params}`, {
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
      "apiOcrVinScanner": 1,
      "apiOemVinLookup": 1,
      "apiStolenCheck": 1,
      "apiVehicleMarketValue": 1,
      "apiVinDecode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiOcrVinScanner` | number | Remaining OCR VIN Scanner credits. |
| `apiOemVinLookup` | number | Remaining OEM VIN Lookup credits. |
| `apiStolenCheck` | number | Remaining Stolen Check credits. |
| `apiVehicleMarketValue` | number | Remaining Vehicle Market Value credits. |
| `apiVinDecode` | number | Remaining VIN Decode credits. |

## Native endpoint

Through the native Vincario API, this operation is `GET /:apiKey/:controlSum/balance.:format` (base URL `https://api.vincario.com/3.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-balance.md) for the provider-specific parameters and requirements.

