# SignalWire: Create SWML Script

Creates a new SWML script in SignalWire.

```
POST https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-swml-script
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-swml-script" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "contents": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-swml-script', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "contents": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Display name of the SWML Script |
| `contents` | string | yes | The contents of the SWML script. |
| `statusCallbackUrl` | string | no | URL to send status callbacks to |

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
      "swml_script": {
        "contents": "string",
        "display_name": "Ava Chen",
        "id": "string",
        "request_url": "https://example.com",
        "status_callback_method": "string",
        "status_callback_url": "https://example.com"
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
| `display_name` | string | Display name of the SWML Script Fabric Resource |
| `id` | string | Unique ID of the SWML Script. |
| `project_id` | string | Unique ID of the Project. |
| `swml_script.contents` | string | The SWML script contents |
| `swml_script.display_name` | string | The displayed name of the SWML scipt |
| `swml_script.id` | string | Unique ID of a SWML Script. |
| `swml_script.request_url` | string | The url where the SWML script is hosted at. |
| `swml_script.status_callback_method` | string | HTTP method to use for status callbacks |
| `swml_script.status_callback_url` | string | URL to send status callbacks to |
| `type` | string | Type of the Fabric Resource |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `POST /fabric/resources/swml_scripts` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-swml-script.md) for the provider-specific parameters and requirements.

