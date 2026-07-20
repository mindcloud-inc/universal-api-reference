# National Weather Service: Get Latest Product By Type And Location

Retrieves the latest text product from National Weather Service by type and location.

```
GET https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/get-latest-product-by-type-and-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a National Weather Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/get-latest-product-by-type-and-location?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/get-latest-product-by-type-and-location?${params}`, {
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
| `locationId` | string | no | NWS text product location identifier, such as TOP. |
| `typeId` | string | no | NWS text product type identifier, such as AFD. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native National Weather Service API returns.

## Native endpoint

Through the native National Weather Service API, this operation is `GET /products/types/:typeId/locations/:locationId/latest` (base URL `https://api.weather.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-product-by-type-and-location.md) for the provider-specific parameters and requirements.

