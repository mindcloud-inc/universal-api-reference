# Revel Digital: List Playlists



```
GET https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-playlists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revel Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-playlists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-playlists?${params}`, {
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
      "calculated_duration": 1,
      "created_by_id": "string",
      "created_on": "string",
      "duration": 1,
      "group_id": "string",
      "group_name": "Ava Chen",
      "id": "string",
      "is_random_start": true,
      "modified_by_id": "string",
      "modified_on": "string",
      "name": "Ava Chen",
      "sources": [
        {}
      ],
      "tags": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calculated_duration` | number |  |
| `created_by_id` | string |  |
| `created_on` | string |  |
| `duration` | number |  |
| `group_id` | string |  |
| `group_name` | string |  |
| `id` | string |  |
| `is_random_start` | boolean |  |
| `modified_by_id` | string |  |
| `modified_on` | string |  |
| `name` | string |  |
| `sources` | array<object> |  |
| `tags` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Revel Digital API, this operation is `GET /playlists` (base URL `https://api.reveldigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-playlists.md) for the provider-specific parameters and requirements.

