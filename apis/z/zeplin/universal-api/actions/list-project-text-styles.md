# Zeplin: List Project Text Styles

Retrieves a list of project text styles from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-project-text-styles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-project-text-styles?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-project-text-styles?${params}`, {
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
| `includeLinkedStyleguides` | boolean | no | Whether to include linked styleguides or not |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": {},
      "created": 1,
      "font_family": "string",
      "font_size": 1,
      "font_stretch": 1,
      "font_style": "string",
      "font_weight": 1,
      "id": "string",
      "line_height": 1,
      "name": "Ava Chen",
      "postscript_name": "Ava Chen",
      "source": {},
      "text_align": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | object |  |
| `created` | number |  |
| `font_family` | string |  |
| `font_size` | number |  |
| `font_stretch` | number |  |
| `font_style` | string |  |
| `font_weight` | number |  |
| `id` | string |  |
| `line_height` | number |  |
| `name` | string |  |
| `postscript_name` | string |  |
| `source` | object |  |
| `text_align` | string |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /projects/{project_id}/text_styles` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-text-styles.md) for the provider-specific parameters and requirements.

