# Umami: Get Event Data Events



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-event-data-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-event-data-events?connectionId=$CONNECTION_ID&websiteId=string&startAt=1&endAt=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "startAt": "1",
  "endAt": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-event-data-events?${params}`, {
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
| `startAt` | number | yes | Timestamp in milliseconds for the start of the reporting range. |
| `endAt` | number | yes | Timestamp in milliseconds for the end of the reporting range. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataType": 1,
      "eventName": "Ava Chen",
      "propertyName": "Ava Chen",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataType` | number | Stored event data type code. |
| `eventName` | string | Tracked event name. |
| `propertyName` | string | Event property name. |
| `total` | number | Count of records for the event-property combination. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/event-data/events` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-data-events.md) for the provider-specific parameters and requirements.

