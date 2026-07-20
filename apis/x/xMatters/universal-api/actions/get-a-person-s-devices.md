# xMatters: Get a person's devices

Retrieves a person's devices from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-person-s-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-person-s-devices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-person-s-devices?${params}`, {
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
| `embed` | string | no |  |
| `personId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "active": "string",
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
          "phoneNumber": "string",
          "priorityThreshold": "string",
          "recipientType": "string",
          "sequence": 1,
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
            "total": 1
          }
        }
      ],
      "links": {
        "self": "https://example.com"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].active` | string |  |
| `data[].defaultDevice` | boolean |  |
| `data[].delay` | number |  |
| `data[].description` | string |  |
| `data[].deviceType` | string |  |
| `data[].emailAddress` | string |  |
| `data[].externallyOwned` | boolean |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].name` | string |  |
| `data[].owner.id` | string |  |
| `data[].owner.links.self` | string |  |
| `data[].owner.targetName` | string |  |
| `data[].phoneNumber` | string |  |
| `data[].priorityThreshold` | string |  |
| `data[].recipientType` | string |  |
| `data[].sequence` | number |  |
| `data[].targetName` | string |  |
| `data[].testStatus` | string |  |
| `data[].timeframes.count` | number |  |
| `data[].timeframes.data[].days[]` | array<string> |  |
| `data[].timeframes.data[].durationInMinutes` | number |  |
| `data[].timeframes.data[].excludeHolidays` | boolean |  |
| `data[].timeframes.data[].name` | string |  |
| `data[].timeframes.data[].startTime` | string |  |
| `data[].timeframes.data[].timezone` | string |  |
| `data[].timeframes.total` | number |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET people/{personId}/devices` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-a-person-s-devices.md) for the provider-specific parameters and requirements.

