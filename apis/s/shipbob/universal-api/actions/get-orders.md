# ShipBob: Get Orders



```
GET https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/get-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipBob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/get-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/get-orders?${params}`, {
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
| `StartDate` | string | no |  |
| `IDs` | string<string> | no | Accepts multiple values as an array. |
| `HasTracking` | string | no |  |
| `isTrackingUploaded` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShipBob API returns.

## Native endpoint

Through the native ShipBob API, this operation is `GET 2026-07/order` (base URL `https://{{credentials.apiSubdomain}}.shipbob.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-orders.md) for the provider-specific parameters and requirements.

