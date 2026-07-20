# PassKit Event Tickets: Get Production Analytics

Retrieves production analytics from PassKit.

```
GET https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-production-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Event Tickets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-production-analytics?connectionId=$CONNECTION_ID&classId=string&protocol=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "classId": "string",
  "protocol": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-production-analytics?${params}`, {
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
| `classId` | string | yes | PassKit production class id for analytics. |
| `protocol` | string | yes | Analytics protocol to report on. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native PassKit Event Tickets API, this operation is `GET /eventTickets/production/:classId/analytics` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-production-analytics.md) for the provider-specific parameters and requirements.

