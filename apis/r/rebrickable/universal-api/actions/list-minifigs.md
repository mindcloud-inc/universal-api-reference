# Rebrickable: List Minifigs

Finds LEGO minifig records in Rebrickable.

```
GET https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-minifigs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrickable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-minifigs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-minifigs?${params}`, {
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
| `search` | string | no | Search term for minifig name or number. |
| `minParts` | number | no | Only return minifigs with at least this many parts. |
| `maxParts` | number | no | Only return minifigs with at most this many parts. |
| `inSetNum` | string | no | Only return minifigs that appear in this set number. |
| `inThemeId` | number | no | Only return minifigs that appear in this theme ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "last_modified_dt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "num_parts": 1,
      "set_img_url": "https://example.com",
      "set_num": "string",
      "set_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `last_modified_dt` | date |  |
| `name` | string |  |
| `num_parts` | number |  |
| `set_img_url` | string |  |
| `set_num` | string |  |
| `set_url` | string |  |

## Native endpoint

Through the native Rebrickable API, this operation is `GET /lego/minifigs/` (base URL `https://rebrickable.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-minifigs.md) for the provider-specific parameters and requirements.

