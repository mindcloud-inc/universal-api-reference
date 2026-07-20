# condoo: Retrieve Pageview

Retrieves a pageview from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-pageview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-pageview?connectionId=$CONNECTION_ID&eventId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-pageview?${params}`, {
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
| `eventId` | number | yes | Required pageview event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browser_language": "string",
      "browser_name": "Ava Chen",
      "browser_timezone": "string",
      "city_name": "Ava Chen",
      "continent_code": "string",
      "country_code": "string",
      "datetime": "2026-05-07T12:00:00.000Z",
      "device_type": "string",
      "expiration_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "last_datetime": "2026-05-07T12:00:00.000Z",
      "os_name": "Ava Chen",
      "path": "string",
      "referrer_host": "string",
      "referrer_path": "string",
      "screen_resolution": "string",
      "theme": "string",
      "type": "string",
      "utm_campaign": "string",
      "utm_medium": "string",
      "utm_source": "string",
      "website_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browser_language` | string |  |
| `browser_name` | string |  |
| `browser_timezone` | string |  |
| `city_name` | string |  |
| `continent_code` | string |  |
| `country_code` | string |  |
| `datetime` | date |  |
| `device_type` | string |  |
| `expiration_date` | date |  |
| `id` | number |  |
| `last_datetime` | date |  |
| `os_name` | string |  |
| `path` | string |  |
| `referrer_host` | string |  |
| `referrer_path` | string |  |
| `screen_resolution` | string |  |
| `theme` | string |  |
| `type` | string |  |
| `utm_campaign` | string |  |
| `utm_medium` | string |  |
| `utm_source` | string |  |
| `website_id` | number |  |

## Native endpoint

Through the native condoo API, this operation is `GET /pageviews-lightweight/{event_id}` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-pageview.md) for the provider-specific parameters and requirements.

