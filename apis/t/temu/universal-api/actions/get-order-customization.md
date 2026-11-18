# Temu: Get Order Customization

Retrieve customized product content information in bulk

```
GET https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-order-customization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-order-customization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-order-customization?${params}`, {
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
| `orderSnList` | string | no | One or more Order Serial Numbers - 'orderSnList["string"]' **Up to 10 Orders can be queried at once.** Accepts multiple values as an array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Temu API returns.

## Native endpoint

Through the native Temu API, this operation is `POST /router` (base URL `https://openapi-b-us.temu.com/openapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-customization.md) for the provider-specific parameters and requirements.

