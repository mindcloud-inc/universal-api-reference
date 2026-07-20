# Webex Interact: Filter shortlinks

Finds shortlinks in Webex Interact by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/filter-shortlinks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/filter-shortlinks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/filter-shortlinks?${params}`, {
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
| `created_at_end` | date | no | Filter shortlinks created before this ISO 8601 timestamp. |
| `created_at_start` | date | no | Filter shortlinks created after this ISO 8601 timestamp. |
| `page_number` | string | no | Page number to return. |
| `page_size` | string | no | Number of shortlinks per page. |
| `query` | string | no | Fuzzy search text for shortlink title or tags. |
| `sort_order` | string | no | Sort order: ASC or DESC. |
| `tags` | list<string> | no | Exact-match tag filters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "paging": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `paging` | object |  |

## Native endpoint

Through the native Webex Interact API, this operation is `POST /assets/v1/shortlink/filter` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/filter-shortlinks.md) for the provider-specific parameters and requirements.

