# Harbour: List Agreements

Retrieves a list of agreements from Harbour.

```
GET https://connect.mindcloud.co/v1/universal/harbour/latest/actions/list-agreements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/list-agreements?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harbour/latest/actions/list-agreements?${params}`, {
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
| `limit` | number | no | Limit results per response. Example: `100`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offset` | number | no | Skip records before this offset. Example: `0`. |
| `order_by` | string | no | Sort field: ID, TITLE, or DATE_CREATED. Example: `DATE_CREATED`. |
| `sort_order` | string | no | Sort direction: ASC or DESC. Example: `DESC`. |
| `is_template` | boolean | no | Filter template agreements when set. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agreements": [
        {}
      ],
      "page": 1,
      "pages": 1,
      "size": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agreements` | array<object> |  |
| `page` | number |  |
| `pages` | number |  |
| `size` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Harbour API, this operation is `GET https://api.harbourshare.com/v1/agreements` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-agreements.md) for the provider-specific parameters and requirements.

