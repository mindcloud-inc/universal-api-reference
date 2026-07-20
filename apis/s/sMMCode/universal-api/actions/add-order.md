# SMMCode: Add Order



```
POST https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/add-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMMCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/add-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "service": "string",
  "link": "https://example.com",
  "quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/add-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "service": "string",
    "link": "https://example.com",
    "quantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `service` | string | yes | Service ID from the SMMCode service list. |
| `link` | string | yes | Link to the page for the order. |
| `quantity` | number | yes | Needed quantity for the order. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `runs` | number | no | Optional runs to deliver when supported by the selected service. |
| `interval` | number | no | Optional interval in minutes when supported by the selected service. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "order": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `order` | number | Created order ID. |

## Native endpoint

Through the native SMMCode API, this operation is `POST /api/v2` (base URL `https://extended.smmcode.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-order.md) for the provider-specific parameters and requirements.

