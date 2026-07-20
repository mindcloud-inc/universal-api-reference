# LabsMobile: Get Country Prices

Retrieves SMS prices for specific countries from LabsMobile.

```
GET https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/get-country-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LabsMobile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/get-country-prices?connectionId=$CONNECTION_ID&countries%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countries[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/get-country-prices?${params}`, {
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
| `countries[]` | array<string> | yes | Country ISO code array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LabsMobile API returns.

## Native endpoint

Through the native LabsMobile API, this operation is `POST /json/prices` (base URL `https://api.labsmobile.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-country-prices.md) for the provider-specific parameters and requirements.

