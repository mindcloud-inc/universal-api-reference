# LionWheel Delivery: Update Visit

Updates an existing visit in LionWheel Delivery.

```
PUT https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/update-visit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LionWheel Delivery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/update-visit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "visitId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/update-visit', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "visitId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driverId` | string | no | Driver to assign to the visit. |
| `visitAt` | string | no | Visit date in LionWheel's expected format. |
| `visitId` | string | yes | The LionWheel visit ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Mutation result message. |

## Native endpoint

Through the native LionWheel Delivery API, this operation is `PUT /visits/:visit_id` (base URL `https://test.lionwheel.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-visit.md) for the provider-specific parameters and requirements.

