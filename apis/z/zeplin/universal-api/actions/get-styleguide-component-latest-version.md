# Zeplin: Get Styleguide Component Latest Version

Retrieves the latest styleguide component version from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-styleguide-component-latest-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-styleguide-component-latest-version?connectionId=$CONNECTION_ID&styleguideId=string&componentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "styleguideId": "string",
  "componentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-styleguide-component-latest-version?${params}`, {
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
| `styleguideId` | string | yes | Styleguide id |
| `componentId` | string | yes | Component id |
| `linkedProject` | string | no | Reference project id |
| `linkedStyleguide` | string | no | Reference styleguide id |
| `includeLinkedStyleguides` | boolean | no | Whether to include linked styleguides or not |

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
      "created": 1,
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
| `created` | number |  |
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

Through the native Zeplin API, this operation is `GET /styleguides/{styleguide_id}/components/{component_id}/versions/latest` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-styleguide-component-latest-version.md) for the provider-specific parameters and requirements.

