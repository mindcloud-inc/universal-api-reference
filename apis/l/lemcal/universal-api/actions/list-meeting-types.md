# Lemcal: List Meeting Types

Retrieves your meeting types from Lemcal.

```
GET https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/list-meeting-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lemcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/list-meeting-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/list-meeting-types?${params}`, {
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
      "color": "string",
      "duration": 1,
      "Id": "string",
      "meetingLink": "https://example.com",
      "meetingLocations": [
        {}
      ],
      "name": "Ava Chen",
      "privacy": "string",
      "status": "string",
      "type": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Configured color hex value. |
| `duration` | number | Meeting duration in minutes. |
| `Id` | string | Lemcal meeting type identifier. |
| `meetingLink` | string | Public link slug for the meeting type. |
| `meetingLocations` | array<object> | Configured meeting locations for the meeting type. |
| `name` | string | Meeting type display name. |
| `privacy` | string | Meeting type privacy setting. |
| `status` | string | Current meeting type status. |
| `type` | string | Lemcal meeting type category. |
| `userId` | string | The Lemcal user who owns the meeting type. |

## Native endpoint

Through the native Lemcal API, this operation is `GET /meetingTypes` (base URL `https://api.lemcal.com/api/lemcal`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-meeting-types.md) for the provider-specific parameters and requirements.

