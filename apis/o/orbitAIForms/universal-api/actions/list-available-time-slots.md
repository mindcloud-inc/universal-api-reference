# Orbit AI (Forms): List Available Time Slots



```
GET https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/list-available-time-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orbit AI (Forms) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/list-available-time-slots?connectionId=$CONNECTION_ID&userId=string&teamId=string&date=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string",
  "teamId": "string",
  "date": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/list-available-time-slots?${params}`, {
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
| `userId` | string | yes |  |
| `teamId` | string | yes |  |
| `date` | date | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event_type": {},
      "slots": [
        {}
      ],
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event_type` | object |  |
| `slots` | array<object> |  |
| `timezone` | string |  |

## Native endpoint

Through the native Orbit AI (Forms) API, this operation is `GET /api/calendar/availability` (base URL `https://orbitforms.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-time-slots.md) for the provider-specific parameters and requirements.

