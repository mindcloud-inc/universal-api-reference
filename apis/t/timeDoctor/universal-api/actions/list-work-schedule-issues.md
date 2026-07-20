# Time Doctor: List Work Schedule Issues

Retrieves work schedule issues from Time Doctor.

```
GET https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-work-schedule-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-work-schedule-issues?connectionId=$CONNECTION_ID&from=2026-04-01T00%3A00%3A00Z&to=2026-04-30T23%3A59%3A59Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-04-01T00:00:00Z",
  "to": "2026-04-30T23:59:59Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-work-schedule-issues?${params}`, {
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
| `from` | string | yes | Example: `2026-04-01T00:00:00Z`. |
| `to` | string | yes | Example: `2026-04-30T23:59:59Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentTagId": "string",
      "currentTagName": "Ava Chen",
      "issues": 1,
      "ratio": 1,
      "shifts": 1,
      "userId": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentTagId` | string |  |
| `currentTagName` | string |  |
| `issues` | number |  |
| `ratio` | number |  |
| `shifts` | number |  |
| `userId` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Time Doctor API, this operation is `GET /api/1.0/work-schedules/issues` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-work-schedule-issues.md) for the provider-specific parameters and requirements.

