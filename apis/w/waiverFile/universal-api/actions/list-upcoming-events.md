# WaiverFile: List Upcoming Events

Retrieves upcoming events from WaiverFile.

```
GET https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-upcoming-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-upcoming-events?connectionId=$CONNECTION_ID&startDateUTC=2026-05-07T12%3A00%3A00.000Z&endDateUTC=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDateUTC": "2026-05-07T12:00:00.000Z",
  "endDateUTC": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-upcoming-events?${params}`, {
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
| `startDateUTC` | date | yes |  |
| `endDateUTC` | date | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_waiverForms": [
        {}
      ],
      "_waivers": [
        {}
      ],
      "_WPObjectStatus": 1,
      "<Category>k__BackingField": {},
      "me": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_waiverForms` | array<object> |  |
| `_waivers` | array<object> |  |
| `_WPObjectStatus` | number |  |
| `<Category>k__BackingField` | object |  |
| `me` | object |  |

## Native endpoint

Through the native WaiverFile API, this operation is `GET /GetUpcomingEvents` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-upcoming-events.md) for the provider-specific parameters and requirements.

