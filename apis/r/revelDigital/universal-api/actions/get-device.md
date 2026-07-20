# Revel Digital: Get Device



```
GET https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/get-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revel Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/get-device?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/get-device?${params}`, {
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
| `id` | string | yes | Unique identifier of the device. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "beacon": {},
      "deactivated": true,
      "device_type": {},
      "encrypted_registration_key": "string",
      "entered_service": "string",
      "group_id": "string",
      "group_name": "Ava Chen",
      "id": "string",
      "in_sync": true,
      "is_online": true,
      "language_code": "string",
      "last_service": "string",
      "last_update": "string",
      "location": {},
      "mac_address": "string",
      "name": "Ava Chen",
      "notes": "string",
      "ping_data": {},
      "registration_key": "string",
      "serial_number": "string",
      "service_level": "string",
      "tags": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `beacon` | object |  |
| `deactivated` | boolean |  |
| `device_type` | object |  |
| `encrypted_registration_key` | string |  |
| `entered_service` | string |  |
| `group_id` | string |  |
| `group_name` | string |  |
| `id` | string |  |
| `in_sync` | boolean |  |
| `is_online` | boolean |  |
| `language_code` | string |  |
| `last_service` | string |  |
| `last_update` | string |  |
| `location` | object |  |
| `mac_address` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `ping_data` | object |  |
| `registration_key` | string |  |
| `serial_number` | string |  |
| `service_level` | string |  |
| `tags` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Revel Digital API, this operation is `GET /devices/:id` (base URL `https://api.reveldigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device.md) for the provider-specific parameters and requirements.

