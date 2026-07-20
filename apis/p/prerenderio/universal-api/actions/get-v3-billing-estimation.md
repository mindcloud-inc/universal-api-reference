# Prerender.io: List Billing Estimation

Retrieves billing estimation from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-billing-estimation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-billing-estimation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-billing-estimation?${params}`, {
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
      "onDemandCost": 1,
      "onDemandRenders": 1,
      "packagesCost": 1,
      "renders": 1,
      "reservedCost": 1,
      "reservedRenders": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `onDemandCost` | number |  |
| `onDemandRenders` | number |  |
| `packagesCost` | number |  |
| `renders` | number |  |
| `reservedCost` | number |  |
| `reservedRenders` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/billing/estimation` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-billing-estimation.md) for the provider-specific parameters and requirements.

