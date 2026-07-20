# ThingsBoard: Get Device

Retrieves a device from ThingsBoard.

```
GET https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-device?connectionId=$CONNECTION_ID&deviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-device?${params}`, {
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
| `deviceId` | string | yes | The ThingsBoard device ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": 1,
      "deviceProfileId": {
        "id": "string"
      },
      "id": {
        "entityType": "string",
        "id": "string"
      },
      "label": "string",
      "name": "Ava Chen",
      "tenantId": {
        "id": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | number |  |
| `deviceProfileId.id` | string |  |
| `id.entityType` | string |  |
| `id.id` | string |  |
| `label` | string |  |
| `name` | string |  |
| `tenantId.id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `GET /device/:deviceId` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device.md) for the provider-specific parameters and requirements.

