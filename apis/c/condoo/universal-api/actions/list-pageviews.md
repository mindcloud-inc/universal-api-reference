# condoo: List Pageviews

Retrieves pageviews from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-pageviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-pageviews?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-pageviews?${params}`, {
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
| `browserLanguage` | string | no | Filter pageviews by browser language. |
| `browserTimezone` | string | no | Filter pageviews by browser timezone. |
| `continentCode` | string | no | Optional continent code selector. |
| `countryCode` | string | no | Optional country code selector. |
| `deviceType` | string | no | Optional device type. Allowed values: desktop, tablet, mobile. |
| `search` | string | no | Optional search string. |
| `searchBy` | string | no | Optional search field. Allowed values: path, referrer_host. |
| `theme` | string | no | Optional theme. Allowed values: light, dark. |
| `type` | string | no | Optional pageview type. Allowed values: pageview, custom. |
| `websiteId` | number | no | Optional website ID selector. |

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

Through the native condoo API, this operation is `GET /pageviews-lightweight/` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pageviews.md) for the provider-specific parameters and requirements.

