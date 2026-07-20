# PubNub: List Applications For Customer

Retrieves applications for a PubNub customer.

```
GET https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/list-applications-for-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PubNub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/list-applications-for-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/list-applications-for-customer?${params}`, {
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
| `customerId` | string | no | PubNub customer ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PubNub API returns.

## Native endpoint

Through the native PubNub API, this operation is `GET /oem/customers/:customerId/applications` (base URL `https://admin-api.pubnub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-applications-for-customer.md) for the provider-specific parameters and requirements.

