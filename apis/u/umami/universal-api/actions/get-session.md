# Umami: Get Session



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-session?connectionId=$CONNECTION_ID&websiteId=string&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-session?${params}`, {
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
| `websiteId` | string | yes | The website ID. |
| `sessionId` | string | yes | The session ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browser": "string",
      "city": "string",
      "country": "string",
      "device": "string",
      "distinctId": "string",
      "events": 1,
      "firstAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "language": "string",
      "lastAt": "2026-05-07T12:00:00.000Z",
      "os": "string",
      "region": "string",
      "screen": "string",
      "totaltime": 1,
      "views": 1,
      "visits": 1,
      "websiteId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browser` | string | Browser name. |
| `city` | string | Visitor city. |
| `country` | string | Visitor country code. |
| `device` | string | Device type. |
| `distinctId` | string | Distinct user identifier when set. |
| `events` | number | Event count in the session. |
| `firstAt` | date | Timestamp of the first activity in the session. |
| `id` | string | Session identifier. |
| `language` | string | Browser language. |
| `lastAt` | date | Timestamp of the last activity in the session. |
| `os` | string | Operating system name. |
| `region` | string | Visitor region code. |
| `screen` | string | Screen resolution. |
| `totaltime` | number | Total tracked time in seconds. |
| `views` | number | Pageview count in the session. |
| `visits` | number | Visit count in the session. |
| `websiteId` | string | Website identifier. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/sessions/:sessionId` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session.md) for the provider-specific parameters and requirements.

