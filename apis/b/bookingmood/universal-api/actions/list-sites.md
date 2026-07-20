# Bookingmood: List Sites

Retrieves site records from the Bookingmood API.

```
GET https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-sites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-sites?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "autocomplete_date_selection": true,
      "color_background": "string",
      "color_primary": "string",
      "color_text": "string",
      "cover": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "custom_domain": "string",
      "filters": [
        "string"
      ],
      "icon": "string",
      "id": "string",
      "logo": "string",
      "name": {},
      "organization_id": "string",
      "show_branding": true,
      "show_searchbar": true,
      "subdomain": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autocomplete_date_selection` | boolean |  |
| `color_background` | string |  |
| `color_primary` | string |  |
| `color_text` | string |  |
| `cover` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `custom_domain` | string |  |
| `filters` | array<string> |  |
| `icon` | string |  |
| `id` | string |  |
| `logo` | string |  |
| `name` | object |  |
| `organization_id` | string |  |
| `show_branding` | boolean |  |
| `show_searchbar` | boolean |  |
| `subdomain` | string |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Bookingmood API, this operation is `GET /sites` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sites.md) for the provider-specific parameters and requirements.

