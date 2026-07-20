# SignalWire: Update cXML Application

Updates an existing cXML application in SignalWire.

```
PUT https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/update-cxml-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/update-cxml-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/update-cxml-application', {
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
| `id` | string | yes | Unique ID of a cXML Application. |
| `displayName` | string | no | Display name of the cXML Application |
| `accountSid` | string | no | Project ID for the cXML Application |
| `voiceUrl` | string | no | URL to handle incoming calls |
| `voiceMethod` | string | no | HTTP method for voice URL |
| `voiceFallbackUrl` | string | no | Fallback URL for voice errors |
| `voiceFallbackMethod` | string | no | HTTP method for voice fallback URL |
| `statusCallback` | string | no | URL to receive status callbacks |
| `statusCallbackMethod` | string | no | HTTP method for status callbacks |
| `smsUrl` | string | no | URL to handle incoming messages |
| `smsMethod` | string | no | HTTP method for SMS URL |
| `smsFallbackUrl` | string | no | Fallback URL for SMS errors |
| `smsFallbackMethod` | string | no | HTTP method for SMS fallback URL |
| `smsStatusCallback` | string | no | URL to receive SMS status callbacks |
| `smsStatusCallbackMethod` | string | no | HTTP method for SMS status callbacks |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "cxml_application": {
        "friendly_name": "Ava Chen",
        "id": "string",
        "project_id": "string",
        "sms_fallback_method": "string",
        "sms_fallback_url": "https://example.com",
        "sms_method": "string",
        "sms_status_callback": "string",
        "sms_status_callback_method": "string",
        "sms_url": "https://example.com",
        "status_callback": "string",
        "status_callback_method": "string",
        "voice_fallback_method": "string",
        "voice_fallback_url": "https://example.com",
        "voice_method": "string",
        "voice_url": "https://example.com"
      },
      "display_name": "Ava Chen",
      "id": "string",
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
| `cxml_application.friendly_name` | string | Display name of the cXML Application |
| `cxml_application.id` | string | Unique ID of the cXML Application. |
| `cxml_application.project_id` | string | Project ID for the cXML Application |
| `cxml_application.sms_fallback_method` | string | HTTP method for SMS fallback URL |
| `cxml_application.sms_fallback_url` | string | Fallback URL for SMS errors |
| `cxml_application.sms_method` | string | HTTP method for SMS URL |
| `cxml_application.sms_status_callback` | string | URL to receive SMS status callbacks |
| `cxml_application.sms_status_callback_method` | string | HTTP method for SMS status callbacks |
| `cxml_application.sms_url` | string | URL to handle incoming messages |
| `cxml_application.status_callback` | string | URL to receive status callbacks |
| `cxml_application.status_callback_method` | string | HTTP method for status callbacks |
| `cxml_application.voice_fallback_method` | string | HTTP method for voice fallback URL |
| `cxml_application.voice_fallback_url` | string | Fallback URL for voice errors |
| `cxml_application.voice_method` | string | HTTP method for voice URL |
| `cxml_application.voice_url` | string | URL to handle incoming calls |
| `display_name` | string | Display name of the cXML Application Fabric Resource |
| `id` | string | Unique ID of the cXML Application. |
| `project_id` | string | Unique ID of the Project. |
| `type` | string | Type of the Fabric Resource |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `PUT /fabric/resources/cxml_applications/{id}` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-cxml-application.md) for the provider-specific parameters and requirements.

