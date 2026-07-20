# SignalWire: List Relay Applications

Retrieves relay applications from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-relay-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-relay-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-relay-applications?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "relay_application": {
        "call_status_callback_url": "https://example.com",
        "id": "string",
        "name": "Ava Chen",
        "topic": "string"
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
| `display_name` | string | Display name of the Relay Application Fabric Resource |
| `id` | string | Unique ID of the Relay Application. |
| `project_id` | string | Unique ID of the Project. |
| `relay_application.call_status_callback_url` | string | Call status callback URL |
| `relay_application.id` | string | Unique ID of a Relay Application. |
| `relay_application.name` | string | Name of the Relay Application |
| `relay_application.topic` | string | Topic of the Relay Application |
| `type` | string | Type of the Fabric Resource |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `GET /fabric/resources/relay_applications` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-relay-applications.md) for the provider-specific parameters and requirements.

