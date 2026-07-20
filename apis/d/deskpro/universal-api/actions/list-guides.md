# Deskpro: List Guides

Retrieves a list of guides from Deskpro.

```
GET https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-guides
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deskpro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-guides?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-guides?${params}`, {
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
      "brand": 1,
      "color": "string",
      "description": "string",
      "displayOrder": 1,
      "iconProperty": 1,
      "id": 1,
      "slug": "string",
      "splashImageProperty": 1,
      "title": "string",
      "topics": [
        1
      ],
      "usergroups": [
        1
      ],
      "useVolumes": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | number | The linked brand ID. |
| `color` | string | The guide color. |
| `description` | string | The guide description. |
| `displayOrder` | number | Display order. |
| `iconProperty` | number | The icon property ID. |
| `id` | number | The unique ID of the guide. |
| `slug` | string | The guide slug. |
| `splashImageProperty` | number | The splash image property ID. |
| `title` | string | The guide title. |
| `topics[]` | number | Topic IDs in the guide. |
| `usergroups[]` | number | Usergroup IDs that can access the guide. |
| `useVolumes` | boolean | Whether the guide uses volumes. |

## Native endpoint

Through the native Deskpro API, this operation is `GET /guides` (base URL `{{credentials.helpdeskUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-guides.md) for the provider-specific parameters and requirements.

