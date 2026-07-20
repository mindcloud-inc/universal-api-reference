# xMatters: Modify a device

Updates a device in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-device', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deviceType` | string | no |  |
| `id` | string | no |  |
| `phoneNumber` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultDevice": true,
      "delay": 1,
      "description": "string",
      "deviceType": "string",
      "externallyOwned": true,
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "owner": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "targetName": "Ava Chen"
      },
      "phoneNumber": "string",
      "priorityThreshold": "string",
      "provider": {
        "id": "string"
      },
      "recipientType": "string",
      "sequence": 1,
      "status": "string",
      "targetName": "Ava Chen",
      "testStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultDevice` | boolean |  |
| `delay` | number |  |
| `description` | string |  |
| `deviceType` | string |  |
| `externallyOwned` | boolean |  |
| `id` | string |  |
| `links.self` | string |  |
| `name` | string |  |
| `owner.id` | string |  |
| `owner.links.self` | string |  |
| `owner.targetName` | string |  |
| `phoneNumber` | string |  |
| `priorityThreshold` | string |  |
| `provider.id` | string |  |
| `recipientType` | string |  |
| `sequence` | number |  |
| `status` | string |  |
| `targetName` | string |  |
| `testStatus` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST devices` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-a-device.md) for the provider-specific parameters and requirements.

