# xMatters: Delete a device

Deletes a device from your xMatters instance.

```
DELETE https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-device?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-device?${params}`, {
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
| `deviceId` | string | no |  |

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
| `recipientType` | string |  |
| `sequence` | number |  |
| `status` | string |  |
| `targetName` | string |  |
| `testStatus` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `DELETE devices/{deviceId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-device.md) for the provider-specific parameters and requirements.

