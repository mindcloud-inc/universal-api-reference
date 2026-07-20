# Zeplin: Get Latest Screen Version

Retrieves the latest screen version from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-latest-screen-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-latest-screen-version?connectionId=$CONNECTION_ID&projectId=string&screenId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "screenId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-latest-screen-version?${params}`, {
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
      "assets": [
        {}
      ],
      "background_color": {},
      "commit": {},
      "creator": {},
      "density_scale": 1,
      "height": 1,
      "id": "string",
      "image_url": "https://example.com",
      "layers": [
        {}
      ],
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
| `assets` | array<object> |  |
| `background_color` | object |  |
| `commit` | object |  |
| `creator` | object |  |
| `density_scale` | number |  |
| `height` | number |  |
| `id` | string |  |
| `image_url` | string |  |
| `layers` | array<object> |  |
| `links` | array<object> |  |
| `source` | string |  |
| `source_file_url` | string |  |
| `thumbnails` | object |  |
| `width` | number |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /projects/{project_id}/screens/{screen_id}/versions/latest` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-screen-version.md) for the provider-specific parameters and requirements.

