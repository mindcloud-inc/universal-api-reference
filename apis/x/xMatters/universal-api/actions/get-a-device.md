# xMatters: Get a device

Retrieves a device from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-device?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-device?${params}`, {
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
| `embed` | string | no |  |

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
      "emailAddress": "ava@example.com",
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
      "priorityThreshold": "string",
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
| `emailAddress` | string |  |
| `externallyOwned` | boolean |  |
| `id` | string |  |
| `links.self` | string |  |
| `name` | string |  |
| `owner.id` | string |  |
| `owner.links.self` | string |  |
| `owner.targetName` | string |  |
| `priorityThreshold` | string |  |
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

Through the native xMatters API, this operation is `GET devices/{deviceId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-device.md) for the provider-specific parameters and requirements.

