# LionWheel Delivery: Find Tasks by Phone

Finds tasks in LionWheel Delivery by phone number.

```
GET https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/find-tasks-by-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LionWheel Delivery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/find-tasks-by-phone?connectionId=$CONNECTION_ID&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/find-tasks-by-phone?${params}`, {
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
| `phone` | string | yes | The recipient phone number to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tasks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tasks` | array<object> | Tasks matching the phone number. |

## Native endpoint

Through the native LionWheel Delivery API, this operation is `GET /tasks/by_phone/:phone` (base URL `https://test.lionwheel.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-tasks-by-phone.md) for the provider-specific parameters and requirements.

