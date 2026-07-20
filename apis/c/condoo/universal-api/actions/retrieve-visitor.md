# condoo: Retrieve Visitor

Retrieves a visitor from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-visitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-visitor?connectionId=$CONNECTION_ID&visitorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "visitorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-visitor?${params}`, {
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
| `visitorId` | string | yes | Required visitor ID or visitor UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browser_language": "string",
      "browser_name": "Ava Chen",
      "browser_timezone": "string",
      "browser_version": "string",
      "city_name": "Ava Chen",
      "continent_code": "string",
      "country_code": "string",
      "custom_parameters": {},
      "date": "2026-05-07T12:00:00.000Z",
      "device_type": "string",
      "goals_conversions_ids": [
        1
      ],
      "id": 1,
      "ip": "string",
      "last_date": "2026-05-07T12:00:00.000Z",
      "last_event_id": 1,
      "os_name": "Ava Chen",
      "os_version": "string",
      "theme": "string",
      "total_sessions": 1,
      "visitor_uuid": "string",
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
| `browser_version` | string |  |
| `city_name` | string |  |
| `continent_code` | string |  |
| `country_code` | string |  |
| `custom_parameters` | object |  |
| `date` | date |  |
| `device_type` | string |  |
| `goals_conversions_ids` | array<number> |  |
| `id` | number |  |
| `ip` | string |  |
| `last_date` | date |  |
| `last_event_id` | number |  |
| `os_name` | string |  |
| `os_version` | string |  |
| `theme` | string |  |
| `total_sessions` | number |  |
| `visitor_uuid` | string |  |
| `website_id` | number |  |

## Native endpoint

Through the native condoo API, this operation is `GET /visitors/{visitor_id}` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-visitor.md) for the provider-specific parameters and requirements.

