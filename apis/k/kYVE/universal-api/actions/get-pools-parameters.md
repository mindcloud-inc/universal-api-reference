# KYVE: Get Pools Parameters



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-pools-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-pools-parameters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-pools-parameters?${params}`, {
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
      "bundles_params": {},
      "funders_params": {},
      "global_params": {},
      "gov_params": {},
      "pool_params": {},
      "stakers_params": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bundles_params` | object |  |
| `funders_params` | object |  |
| `global_params` | object |  |
| `gov_params` | object |  |
| `pool_params` | object |  |
| `stakers_params` | object |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/query/v1beta1/params` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pools-parameters.md) for the provider-specific parameters and requirements.

