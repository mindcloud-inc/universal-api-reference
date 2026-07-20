# Notion: Retrieve Page Property Item

Retrieves a page property item from Notion.

```
GET https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-page-property-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-page-property-item?connectionId=$CONNECTION_ID&page_id=string&property_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page_id": "string",
  "property_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-page-property-item?${params}`, {
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
| `page_id` | string | yes |  |
| `property_id` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startCursor` | string | no |  |
| `pageSize` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "id": "string",
      "nextCursor": "string",
      "nextUrl": "https://example.com",
      "object": "string",
      "propertyItem": {},
      "results": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean |  |
| `id` | string |  |
| `nextCursor` | string |  |
| `nextUrl` | string |  |
| `object` | string |  |
| `propertyItem` | object |  |
| `results` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Notion API, this operation is `GET /pages/:page_id/properties/:property_id` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-page-property-item.md) for the provider-specific parameters and requirements.

