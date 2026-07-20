# Bureau of Economic Analysis: Get Parameter List

Retrieves parameters for a Bureau of Economic Analysis dataset.

```
GET https://connect.mindcloud.co/v1/universal/bureauOfEconomicAnalysis/latest/actions/get-parameter-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bureau of Economic Analysis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bureauOfEconomicAnalysis/latest/actions/get-parameter-list?connectionId=$CONNECTION_ID&dataset_name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset_name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bureauOfEconomicAnalysis/latest/actions/get-parameter-list?${params}`, {
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
| `dataset_name` | string | yes | BEA dataset name, such as NIPA, Regional, or GDPbyIndustry. |

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

Through the native Bureau of Economic Analysis API, this operation is `GET /data` (base URL `https://apps.bea.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-parameter-list.md) for the provider-specific parameters and requirements.

