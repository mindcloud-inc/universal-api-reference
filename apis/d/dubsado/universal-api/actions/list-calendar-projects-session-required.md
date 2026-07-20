# Dubsado: List Calendar Projects (Session Required)



```
GET https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-calendar-projects-session-required
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dubsado `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-calendar-projects-session-required?connectionId=$CONNECTION_ID&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-calendar-projects-session-required?${params}`, {
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
| `startDate` | date | yes | Start date for the calendar project window. |
| `endDate` | date | yes | End date for the calendar project window. |
| `limit` | number | no | Optional result limit observed in the Dubsado app bundle for /calendar/project reads. |
| `job` | string | no | Optional project ID filter for /calendar/project reads. |
| `client` | string | no | Optional client ID filter for /calendar/project reads. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dubsado API returns.

## Native endpoint

Through the native Dubsado API, this operation is `GET /calendar/project` (base URL `https://app.dubsado.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendar-projects-session-required.md) for the provider-specific parameters and requirements.

