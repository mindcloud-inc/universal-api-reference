# Rebrickable: List Parts

Finds LEGO part records in Rebrickable.

```
GET https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-parts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrickable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-parts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-parts?${params}`, {
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
| `search` | string | no | Search term for part name or number. |
| `partNum` | string | no | Filter by one exact Rebrickable part number. |
| `partNums` | string | no | Comma-separated Rebrickable part numbers to fetch together. |
| `partCatId` | number | no | Only return parts in this Rebrickable part category. |
| `colorId` | number | no | Only return parts in this Rebrickable color. |
| `bricklinkId` | string | no | Filter by BrickLink part ID. |
| `brickowlId` | string | no | Filter by BrickOwl part ID. |
| `legoId` | string | no | Filter by LEGO element or design ID. |
| `ldrawId` | string | no | Filter by LDraw part ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "external_ids": {},
      "name": "Ava Chen",
      "part_cat_id": 1,
      "part_img_url": "https://example.com",
      "part_num": "string",
      "part_url": "https://example.com",
      "print_of": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `external_ids` | object |  |
| `name` | string |  |
| `part_cat_id` | number |  |
| `part_img_url` | string |  |
| `part_num` | string |  |
| `part_url` | string |  |
| `print_of` | string |  |

## Native endpoint

Through the native Rebrickable API, this operation is `GET /lego/parts/` (base URL `https://rebrickable.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-parts.md) for the provider-specific parameters and requirements.

