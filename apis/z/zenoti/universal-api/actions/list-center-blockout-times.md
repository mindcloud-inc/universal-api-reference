# Zenoti: List Center Blockout Times



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-center-blockout-times
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-center-blockout-times?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-center-blockout-times?${params}`, {
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
| `startDate` | date | no |  |
| `endDate` | date | no |  |
| `centerId` | list | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockOutTimeId": "string",
      "blockOutTimeType": {
        "duration": 1,
        "id": 1,
        "name": "Ava Chen"
      },
      "employee": {
        "id": "string",
        "name": "Ava Chen"
      },
      "endTime": "string",
      "endTimeInCenter": "string",
      "notes": "string",
      "recurringBlockOutTime": {},
      "room": {},
      "startTime": "string",
      "startTimeInCenter": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockOutTimeId` | string |  |
| `blockOutTimeType.duration` | number |  |
| `blockOutTimeType.id` | number |  |
| `blockOutTimeType.name` | string |  |
| `employee.id` | string |  |
| `employee.name` | string |  |
| `endTime` | string |  |
| `endTimeInCenter` | string |  |
| `notes` | string |  |
| `recurringBlockOutTime` | object |  |
| `room` | object |  |
| `startTime` | string |  |
| `startTimeInCenter` | string |  |

## Native endpoint

Through the native Zenoti API, this operation is `GET centers/:centerId/blockouttimes` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-center-blockout-times.md) for the provider-specific parameters and requirements.

