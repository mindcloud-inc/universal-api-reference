# Hyperzod: Retrieve Order Scheduling Slots

Retrieves order scheduling slots from Hyperzod.

```
GET https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/retrieve-order-scheduling-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperzod `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/retrieve-order-scheduling-slots?connectionId=$CONNECTION_ID&merchantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "merchantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/retrieve-order-scheduling-slots?${params}`, {
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
| `merchantId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the Hyperzod request completed successfully. |

## Native endpoint

Through the native Hyperzod API, this operation is `GET /admin/v1/order/scheduling-slots` (base URL `https://api.hyperzod.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order-scheduling-slots.md) for the provider-specific parameters and requirements.

