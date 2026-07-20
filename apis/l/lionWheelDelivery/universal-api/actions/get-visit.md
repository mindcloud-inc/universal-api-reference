# LionWheel Delivery: Get Visit

Retrieves a visit from LionWheel Delivery.

```
GET https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/get-visit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LionWheel Delivery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/get-visit?connectionId=$CONNECTION_ID&visitId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "visitId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/get-visit?${params}`, {
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
| `visitId` | string | yes | The LionWheel visit ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "visit": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `visit` | object | The requested LionWheel visit. |

## Native endpoint

Through the native LionWheel Delivery API, this operation is `GET /visits/:visit_id` (base URL `https://test.lionwheel.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-visit.md) for the provider-specific parameters and requirements.

