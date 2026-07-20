# Tallyfy: List Tags

Retrieves tags from your Tallyfy organization.

```
GET https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tallyfy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/list-tags?${params}`, {
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
      "active_process": 1,
      "auto_generated": true,
      "color": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "template": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_process` | number |  |
| `auto_generated` | boolean |  |
| `color` | string |  |
| `created_at` | date |  |
| `deleted_at` | date |  |
| `id` | string |  |
| `template` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Tallyfy API, this operation is `GET /organizations/:org/tags` (base URL `https://api.tallyfy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

