# DatoCMS: List Items



```
GET https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-items?${params}`, {
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
| `filterQuery` | string | no | Text query applied to searchable fields. Example: `marketing`. |
| `filterType` | string | no | Filter items by item type ID. Example: `blog_post`. |
| `nested` | boolean | no | Include nested objects in the response payload when available. Example: `true`. |
| `version` | string | no | Select content version, for example current or published. Example: `current`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locale` | string | no | Locale used for localized filtering and ordering. Example: `en`. |
| `filterIds` | string | no | Comma-separated item IDs to return. Example: `123,456`. |
| `onlyValid` | string | no | When set, only valid records are returned. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "meta": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Item fields |
| `id` | string | Item ID |
| `meta` | object | State metadata |
| `relationships` | object | Linked resources |
| `type` | string | Resource type |

## Native endpoint

Through the native DatoCMS API, this operation is `GET /items` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

