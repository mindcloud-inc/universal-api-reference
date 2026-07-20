# AntsRoute: Get Order Tracking Link

Retrieves an order tracking link from AntsRoute by ID.

```
GET https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/get-order-tracking-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AntsRoute `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/get-order-tracking-link?connectionId=$CONNECTION_ID&id=1&language=en_GB" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "language": "en_GB"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/get-order-tracking-link?${params}`, {
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
| `id` | number | yes |  |
| `language` | string | yes | Required language enum for the tracking page. Use one of `en_GB`, `fr_FR`, `es_ES`, `de_DE`, `it_IT`, or `nl_NL`. Default: `en_GB`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AntsRoute API returns.

## Native endpoint

Through the native AntsRoute API, this operation is `GET /capi/order/id/:id/tracking-link` (base URL `https://app.antsroute.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-tracking-link.md) for the provider-specific parameters and requirements.

