# Placid: List Templates

Finds templates in Placid by collection, title, or tag.

```
GET https://connect.mindcloud.co/v1/universal/placid/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placid/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placid/latest/actions/list-templates?${params}`, {
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
| `collectionId` | string | no | Only return templates from the specified collection. |
| `titleFilter` | string | no | Only return templates whose title matches the filter. |
| `orderBy` | string | no | Sort templates using the documented order_by format, for example created_at-asc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collections": [
        "string"
      ],
      "customData": "string",
      "height": 1,
      "layers": [
        {}
      ],
      "tags": [
        "string"
      ],
      "thumbnail": "string",
      "title": "string",
      "uuid": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collections` | array<string> |  |
| `customData` | string |  |
| `height` | number |  |
| `layers` | array<object> |  |
| `tags` | array<string> |  |
| `thumbnail` | string |  |
| `title` | string |  |
| `uuid` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Placid API, this operation is `GET /api/rest/templates` (base URL `https://api.placid.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

