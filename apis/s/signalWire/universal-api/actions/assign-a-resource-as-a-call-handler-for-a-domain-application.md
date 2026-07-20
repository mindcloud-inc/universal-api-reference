# SignalWire: Assign a resource as a call handler for a Domain Application.

Assigns a resource as a call handler for a domain application in SignalWire.

```
PUT https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/assign-a-resource-as-a-call-handler-for-a-domain-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/assign-a-resource-as-a-call-handler-for-a-domain-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "domainApplicationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/assign-a-resource-as-a-call-handler-for-a-domain-application', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "domainApplicationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique identifier of the Resource. |
| `domainApplicationId` | string | yes | The id of the domain application you wish to assign a resource to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": {
        "audio": "string"
      },
      "cover_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
      "id": "string",
      "locked": true,
      "name": "Ava Chen",
      "preview_url": "https://example.com",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels.audio` | string | Audio Channel of Fabric Address |
| `cover_url` | string | Cover url of the Fabric Address. |
| `created_at` | date | Fabric Address Creation Date. |
| `display_name` | string | Display name of the Fabric Address. |
| `id` | string | Unique ID of the Fabric Address. |
| `locked` | boolean | Locks the Fabric Address. This is used to prevent the Fabric Address from accepting calls. |
| `name` | string | Name of the Fabric Address. |
| `preview_url` | string | Preview url of the Fabric Address. |
| `type` | string | The display type of a fabric address pointing to an application. |

## Native endpoint

Through the native SignalWire API, this operation is `POST /fabric/resources/{id}/domain_applications` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-a-resource-as-a-call-handler-for-a-domain-application.md) for the provider-specific parameters and requirements.

