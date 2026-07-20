# DateX (Legacy): Save Shipping Label



```
POST https://connect.mindcloud.co/v1/universal/dateX/latest/actions/save-shipping-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX (Legacy) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dateX/latest/actions/save-shipping-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dateX/latest/actions/save-shipping-label', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `containers[]` | array | no |  |
| `containers[].order_id` | number | no |  |
| `containers[].shipment_id` | string | no |  |
| `containers[].shipping_container` | string | no |  |
| `containers[].ship_label_zpl` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DateX (Legacy) API returns.

## Native endpoint

Through the native DateX (Legacy) API, this operation is `POST packsize/save_shipping_label` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-shipping-label.md) for the provider-specific parameters and requirements.

