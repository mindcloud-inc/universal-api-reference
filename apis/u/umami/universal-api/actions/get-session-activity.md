# Umami: Get Session Activity



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-session-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-session-activity?connectionId=$CONNECTION_ID&websiteId=string&sessionId=string&startAt=1&endAt=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "sessionId": "string",
  "startAt": "1",
  "endAt": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-session-activity?${params}`, {
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
| `startAt` | number | yes | Timestamp in milliseconds for the start of the reporting range. |
| `endAt` | number | yes | Timestamp in milliseconds for the end of the reporting range. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "eventId": "string",
      "eventName": "Ava Chen",
      "eventType": 1,
      "hasData": 1,
      "referrerDomain": "string",
      "urlPath": "https://example.com",
      "urlQuery": "https://example.com",
      "visitId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Timestamp of the activity entry. |
| `eventId` | string | Associated event identifier. |
| `eventName` | string | Event name when present. |
| `eventType` | number | Event type code. |
| `hasData` | number | Whether the activity entry has attached event data. |
| `referrerDomain` | string | Referrer domain. |
| `urlPath` | string | Tracked URL path. |
| `urlQuery` | string | Tracked URL query string. |
| `visitId` | string | Visit identifier. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/sessions/:sessionId/activity` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-activity.md) for the provider-specific parameters and requirements.

