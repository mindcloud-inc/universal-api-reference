# xMatters: Create a device

Creates a device in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-device', {
  method: 'POST',
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
| `defaultDevice` | boolean | no |  |
| `delay` | number | no |  |
| `deviceType` | string | no |  |
| `name` | string | no |  |
| `owner` | string | no |  |
| `phoneNumber` | string | no |  |
| `priorityThreshold` | string | no |  |
| `recipientType` | string | no |  |
| `sequence` | number | no |  |
| `testStatus` | string | no |  |
| `timeframes` | list<string> | no |  |

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
      "privileged": true,
      "provider": {
        "id": "string"
      },
      "recipientType": "string",
      "sequence": 1,
      "status": "string",
      "targetName": "Ava Chen",
      "testStatus": "string",
      "timeframes": {
        "count": 1,
        "data": [
          {
            "days": [
              [
                "string"
              ]
            ],
            "durationInMinutes": 1,
            "excludeHolidays": true,
            "name": "Ava Chen",
            "startTime": "string",
            "timezone": "string"
          }
        ],
        "links": {
          "self": "https://example.com"
        },
        "total": 1
      }
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
| `privileged` | boolean |  |
| `provider.id` | string |  |
| `recipientType` | string |  |
| `sequence` | number |  |
| `status` | string |  |
| `targetName` | string |  |
| `testStatus` | string |  |
| `timeframes.count` | number |  |
| `timeframes.data[].days[]` | array<string> |  |
| `timeframes.data[].durationInMinutes` | number |  |
| `timeframes.data[].excludeHolidays` | boolean |  |
| `timeframes.data[].name` | string |  |
| `timeframes.data[].startTime` | string |  |
| `timeframes.data[].timezone` | string |  |
| `timeframes.links.self` | string |  |
| `timeframes.total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `POST devices` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-device.md) for the provider-specific parameters and requirements.

