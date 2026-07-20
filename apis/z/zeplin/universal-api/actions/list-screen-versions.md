# Zeplin: List Screen Versions

Retrieves a list of screen versions from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-versions?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string&screenId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string",
  "screenId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-screen-versions?${params}`, {
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
| `projectId` | string | yes | Project id |
| `screenId` | string | yes | Screen id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "background_color": {},
      "commit": {},
      "creator": {},
      "density_scale": 1,
      "height": 1,
      "id": "string",
      "image_url": "https://example.com",
      "links": [
        {}
      ],
      "source": "string",
      "source_file_url": "https://example.com",
      "thumbnails": {},
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background_color` | object |  |
| `commit` | object |  |
| `creator` | object |  |
| `density_scale` | number |  |
| `height` | number |  |
| `id` | string |  |
| `image_url` | string |  |
| `links` | array<object> |  |
| `source` | string |  |
| `source_file_url` | string |  |
| `thumbnails` | object |  |
| `width` | number |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /projects/{project_id}/screens/{screen_id}/versions` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-screen-versions.md) for the provider-specific parameters and requirements.

