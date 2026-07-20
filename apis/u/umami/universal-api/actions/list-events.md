# Umami: List Events



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0&websiteId=string&startAt=1&endAt=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "websiteId": "string",
  "startAt": "1",
  "endAt": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-events?${params}`, {
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
| `startAt` | number | no | Start timestamp in milliseconds. |
| `startAt` | number | yes | Timestamp in milliseconds for the start of the reporting range. |
| `endAt` | number | no | End timestamp in milliseconds. |
| `endAt` | number | yes | Timestamp in milliseconds for the end of the reporting range. |
| `search` | string | no | Optional search text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browser": "string",
      "city": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "device": "string",
      "eventName": "Ava Chen",
      "eventType": 1,
      "hasData": 1,
      "hostname": "Ava Chen",
      "id": "string",
      "os": "string",
      "pageTitle": "string",
      "referrerDomain": "string",
      "referrerPath": "string",
      "referrerQuery": "string",
      "sessionId": "string",
      "urlPath": "https://example.com",
      "urlQuery": "https://example.com",
      "websiteId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browser` | string | Browser. |
| `city` | string | City. |
| `country` | string | Country code. |
| `createdAt` | date | Event timestamp. |
| `device` | string | Device type. |
| `eventName` | string | Event name. |
| `eventType` | number | Event type code. |
| `hasData` | number | Whether event data is attached. |
| `hostname` | string | Hostname. |
| `id` | string | Event row ID. |
| `os` | string | Operating system. |
| `pageTitle` | string | Page title. |
| `referrerDomain` | string | Referrer domain. |
| `referrerPath` | string | Referrer path. |
| `referrerQuery` | string | Referrer query string. |
| `sessionId` | string | Session ID. |
| `urlPath` | string | Page path. |
| `urlQuery` | string | Page query string. |
| `websiteId` | string | Website ID. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/events` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

