# Lemcal: Get Meeting Type

Retrieves a meeting type from Lemcal.

```
GET https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/get-meeting-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lemcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/get-meeting-type?connectionId=$CONNECTION_ID&_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/get-meeting-type?${params}`, {
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
| `_id` | string | yes | The ID of the meeting type to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "color": "string",
      "duration": 1,
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
| `_id` | string |  |
| `color` | string |  |
| `duration` | number |  |
| `meetingLink` | string |  |
| `meetingLocations` | array<object> |  |
| `name` | string |  |
| `privacy` | string |  |
| `status` | string |  |
| `type` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Lemcal API, this operation is `GET /meetingTypes/:_id` (base URL `https://api.lemcal.com/api/lemcal`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting-type.md) for the provider-specific parameters and requirements.

