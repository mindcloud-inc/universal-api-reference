# SignalWire: Get Subscriber

Retrieves a subscriber from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-subscriber?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-subscriber?${params}`, {
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
| `id` | string | yes | Unique ID of a Subscriber. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
      "id": "string",
      "project_id": "string",
      "subscriber": {
        "company_name": "Ava Chen",
        "country": "string",
        "display_name": "Ava Chen",
        "email": "ava@example.com",
        "first_name": "Ava",
        "id": "string",
        "job_title": "string",
        "last_name": "Chen",
        "region": "string",
        "timezone": "string"
      },
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Date and time when the resource was created. |
| `display_name` | string | Display name of the Subscriber. |
| `id` | string | Unique ID of the request. |
| `project_id` | string | Unique ID of the project. |
| `subscriber.company_name` | string | Company name of the Subscriber. |
| `subscriber.country` | string | Country of the Subscriber. |
| `subscriber.display_name` | string | Display name of the Subscriber. |
| `subscriber.email` | string | Email of the Subscriber. |
| `subscriber.first_name` | string | First name of the Subscriber. |
| `subscriber.id` | string | Unique ID of the Subscriber. |
| `subscriber.job_title` | string | Job title of the Subscriber. |
| `subscriber.last_name` | string | Last name of the Subscriber. |
| `subscriber.region` | string | Region of the Subscriber. |
| `subscriber.timezone` | string | Timezone of the Subscriber. |
| `type` | string | Type of the resource. |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `GET /fabric/resources/subscribers/{id}` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber.md) for the provider-specific parameters and requirements.

