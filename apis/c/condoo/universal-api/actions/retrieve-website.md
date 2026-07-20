# condoo: Retrieve Website

Retrieves a website from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-website?connectionId=$CONNECTION_ID&websiteId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-website?${params}`, {
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
| `websiteId` | number | yes | Required website ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bot_exclusion_is_enabled": true,
      "datetime": "2026-05-07T12:00:00.000Z",
      "email_reports_is_enabled": true,
      "email_reports_last_date": "2026-05-07T12:00:00.000Z",
      "events_children_is_enabled": true,
      "excluded_ips": "string",
      "host": "string",
      "id": 1,
      "ip_storage_is_enabled": true,
      "is_enabled": true,
      "last_datetime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "outbound_clicks_is_enabled": true,
      "path": "string",
      "pixel_key": "string",
      "public_statistics_is_enabled": true,
      "public_statistics_password": "string",
      "query_parameters_tracking_is_enabled": true,
      "scheme": "string",
      "sessions_replays_is_enabled": true,
      "tracking_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bot_exclusion_is_enabled` | boolean |  |
| `datetime` | date |  |
| `email_reports_is_enabled` | boolean |  |
| `email_reports_last_date` | date |  |
| `events_children_is_enabled` | boolean |  |
| `excluded_ips` | string |  |
| `host` | string |  |
| `id` | number |  |
| `ip_storage_is_enabled` | boolean |  |
| `is_enabled` | boolean |  |
| `last_datetime` | date |  |
| `name` | string |  |
| `outbound_clicks_is_enabled` | boolean |  |
| `path` | string |  |
| `pixel_key` | string |  |
| `public_statistics_is_enabled` | boolean |  |
| `public_statistics_password` | string |  |
| `query_parameters_tracking_is_enabled` | boolean |  |
| `scheme` | string |  |
| `sessions_replays_is_enabled` | boolean |  |
| `tracking_type` | string |  |

## Native endpoint

Through the native condoo API, this operation is `GET /websites/{website_id}` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-website.md) for the provider-specific parameters and requirements.

