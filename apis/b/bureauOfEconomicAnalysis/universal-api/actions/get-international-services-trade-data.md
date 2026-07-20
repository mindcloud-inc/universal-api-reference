# Bureau of Economic Analysis: Get International Services Trade Data

Retrieves international services trade data from the Bureau of Economic Analysis.

```
GET https://connect.mindcloud.co/v1/universal/bureauOfEconomicAnalysis/latest/actions/get-international-services-trade-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bureau of Economic Analysis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bureauOfEconomicAnalysis/latest/actions/get-international-services-trade-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bureauOfEconomicAnalysis/latest/actions/get-international-services-trade-data?${params}`, {
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
      "BEAAPI": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BEAAPI` | object | BEA API response envelope containing Request and Results. |

## Native endpoint

Through the native Bureau of Economic Analysis API, this operation is `GET /data` (base URL `https://apps.bea.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-international-services-trade-data.md) for the provider-specific parameters and requirements.

