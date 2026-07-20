# ThingsBoard: Save Device

Creates or updates a device in ThingsBoard.

```
PUT https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/save-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/save-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/save-device', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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

Through the native ThingsBoard API, this operation is `POST /device` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-device.md) for the provider-specific parameters and requirements.

