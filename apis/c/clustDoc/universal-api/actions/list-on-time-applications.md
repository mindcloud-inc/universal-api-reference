# ClustDoc: List On-Time Applications



```
GET https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-on-time-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-on-time-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-on-time-applications?${params}`, {
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
      "contact": {},
      "created_at": "string",
      "id": 1,
      "is_late": true,
      "progress_percentage": 1,
      "public_url": "https://example.com",
      "status": "string",
      "status_color": "string",
      "status_string": "string",
      "team": {},
      "template": {},
      "template_id": 1,
      "title": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object |  |
| `created_at` | string |  |
| `id` | number |  |
| `is_late` | boolean |  |
| `progress_percentage` | number |  |
| `public_url` | string |  |
| `status` | string |  |
| `status_color` | string |  |
| `status_string` | string |  |
| `team` | object |  |
| `template` | object |  |
| `template_id` | number |  |
| `title` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `GET /dossiers` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-on-time-applications.md) for the provider-specific parameters and requirements.

