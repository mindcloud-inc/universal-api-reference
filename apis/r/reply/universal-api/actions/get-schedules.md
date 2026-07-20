# Reply: Get Schedules



```
GET https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-schedules?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "isDefault": true,
      "mainTimings": [
        {
          "isActive": true,
          "timeRanges": [
            {
              "fromTime": {
                "hour": 1,
                "minute": 1
              },
              "toTime": {
                "hour": 1,
                "minute": 1
              }
            }
          ],
          "weekDay": "string"
        }
      ],
      "name": "Ava Chen",
      "timezoneId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isDefault` | boolean |  |
| `mainTimings[].isActive` | boolean |  |
| `mainTimings[].timeRanges[].fromTime.hour` | number |  |
| `mainTimings[].timeRanges[].fromTime.minute` | number |  |
| `mainTimings[].timeRanges[].toTime.hour` | number |  |
| `mainTimings[].timeRanges[].toTime.minute` | number |  |
| `mainTimings[].weekDay` | string |  |
| `name` | string |  |
| `timezoneId` | string |  |

## Native endpoint

Through the native Reply API, this operation is `GET /v2/schedules` (base URL `https://api.reply.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedules.md) for the provider-specific parameters and requirements.

