# Umami: Get Event Data



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-event-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-event-data?connectionId=$CONNECTION_ID&websiteId=string&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-event-data?${params}`, {
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
| `eventId` | string | yes | The event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dataKey": "string",
      "dataType": 1,
      "dateValue": "2026-05-07T12:00:00.000Z",
      "eventId": "string",
      "eventName": "Ava Chen",
      "numberValue": 1,
      "sessionId": "string",
      "stringValue": "string",
      "urlPath": "https://example.com",
      "websiteId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Timestamp when the property record was created. |
| `dataKey` | string | Event data property key. |
| `dataType` | number | Stored data type code. |
| `dateValue` | date | Stored date value for the property. |
| `eventId` | string | Event identifier. |
| `eventName` | string | Tracked event name. |
| `numberValue` | number | Stored numeric value for the property. |
| `sessionId` | string | Session identifier associated with the event. |
| `stringValue` | string | Stored string value for the property. |
| `urlPath` | string | Tracked URL path. |
| `websiteId` | string | Website identifier. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/event-data/:eventId` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-data.md) for the provider-specific parameters and requirements.

