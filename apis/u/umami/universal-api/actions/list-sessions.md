# Umami: List Sessions



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0&websiteId=string&startAt=1&endAt=1" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-sessions?${params}`, {
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
      "firstAt": "2026-05-07T12:00:00.000Z",
      "hostname": "Ava Chen",
      "id": "string",
      "language": "string",
      "lastAt": "2026-05-07T12:00:00.000Z",
      "os": "string",
      "region": "string",
      "screen": "string",
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
| `browser` | string | Browser. |
| `city` | string | City. |
| `country` | string | Country code. |
| `createdAt` | date | Creation timestamp. |
| `device` | string | Device type. |
| `firstAt` | date | First seen timestamp. |
| `hostname` | string | Hostname. |
| `id` | string | Session ID. |
| `language` | string | Browser language. |
| `lastAt` | date | Last seen timestamp. |
| `os` | string | Operating system. |
| `region` | string | Region code. |
| `screen` | string | Screen resolution. |
| `views` | number | View count. |
| `visits` | number | Visit count. |
| `websiteId` | string | Website ID. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/sessions` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sessions.md) for the provider-specific parameters and requirements.

