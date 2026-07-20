# Hiboutik: List Calendar Events

Retrieves calendar events for a specific date in Hiboutik.

```
GET https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-calendar-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hiboutik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-calendar-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-calendar-events?${params}`, {
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
| `day` | string | no | The numeric day. |
| `month` | string | no | The numeric month. |
| `storeId` | string | no | The Hiboutik store id. |
| `year` | string | no | The four-digit year. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "eventId": 1,
      "startDate": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string |  |
| `eventId` | number |  |
| `startDate` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Hiboutik API, this operation is `GET /calendar/events/:store_id/:year/:month/:day` (base URL `https://mindcloudhiboutik20260402.hiboutik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendar-events.md) for the provider-specific parameters and requirements.

