# SignalWire: Update cXML Script

Updates an existing cXML script in SignalWire.

```
PUT https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/update-cxml-script
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/update-cxml-script" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/update-cxml-script', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique ID of a cXML Script. |
| `displayName` | string | no | Display name of the cXML Script |
| `contents` | string | no | The cXML script contents |
| `statusCallbackUrl` | string | no | URL to send status callbacks to |
| `statusCallbackMethod` | string | no | HTTP method to use for status callbacks |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "cxml_script": {
        "contents": "string",
        "display_name": "Ava Chen",
        "id": "string",
        "last_accessed_at": "2026-05-07T12:00:00.000Z",
        "request_count": 1,
        "request_url": "https://example.com",
        "script_type": "string",
        "status_callback_method": "string",
        "status_callback_url": "https://example.com"
      },
      "id": "string",
      "name": "Ava Chen",
      "project_id": "string",
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
| `cxml_script.contents` | string | The cXML script contents |
| `cxml_script.display_name` | string | Display name of the cXML Script Fabric Resource |
| `cxml_script.id` | string | Unique ID of a cXML Script. |
| `cxml_script.last_accessed_at` | date | The date and time when the cXML script was last accessed |
| `cxml_script.request_count` | number | The amout of times the cXML script has been requested |
| `cxml_script.request_url` | string | The URL where the cXML script can be accessed |
| `cxml_script.script_type` | string | The script type the cXML Script is used for |
| `cxml_script.status_callback_method` | string | HTTP method for status callback URL |
| `cxml_script.status_callback_url` | string | The url that will send status updates for the cXML Script |
| `id` | string | Unique ID of the cXML Script. |
| `name` | string | Display name of the cXML Script Fabric Resource |
| `project_id` | string | Unique ID of the Project. |
| `type` | string | Type of the Fabric Resource |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `PUT /fabric/resources/cxml_scripts/{id}` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-cxml-script.md) for the provider-specific parameters and requirements.

