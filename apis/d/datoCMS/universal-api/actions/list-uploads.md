# DatoCMS: List Uploads



```
GET https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-uploads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-uploads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-uploads?${params}`, {
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
| `searchQuery` | string | no | Textual query used to search uploads. Example: `foobar`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uploadIds` | string | no | Comma-separated upload IDs to fetch. Example: `12,31`. |
| `filterLocale` | string | no | Locale used when text query or field filters are provided. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Upload attributes |
| `id` | string | Upload ID |
| `type` | string | Resource type |

## Native endpoint

Through the native DatoCMS API, this operation is `GET /uploads` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-uploads.md) for the provider-specific parameters and requirements.

