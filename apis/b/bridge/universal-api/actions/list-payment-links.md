# Bridge: List Payment Links

Retrieves payment links from Bridge.

```
GET https://connect.mindcloud.co/v1/universal/bridge/latest/actions/list-payment-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/list-payment-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridge/latest/actions/list-payment-links?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `after` | string | no | Cursor pointing to the start of the desired set |
| `since` | date | no | Limit to payment links created after the specified date. Format example: 2024-09-21T22:00:00.000Z |
| `until` | date | no | Limit to payment links created before the specified date. Format example: 2024-09-21T22:00:00.000Z |
| `status` | string | no | You can filter payment links by status |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridge API returns.

## Native endpoint

Through the native Bridge API, this operation is `GET /payment/payment-links` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-links.md) for the provider-specific parameters and requirements.

