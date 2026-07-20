# Rebrickable: List Sets Containing Part Color

Retrieves sets containing a LEGO part color in Rebrickable.

```
GET https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-sets-containing-part-color
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrickable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-sets-containing-part-color?connectionId=$CONNECTION_ID&limit=25&offset=0&partNum=string&colorId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "partNum": "string",
  "colorId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-sets-containing-part-color?${params}`, {
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
| `partNum` | string | yes | Rebrickable part number. |
| `colorId` | number | yes | Rebrickable color ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "num_parts": 1,
      "set_img_url": "https://example.com",
      "set_num": "string",
      "set_url": "https://example.com",
      "theme_id": 1,
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `num_parts` | number |  |
| `set_img_url` | string |  |
| `set_num` | string |  |
| `set_url` | string |  |
| `theme_id` | number |  |
| `year` | number |  |

## Native endpoint

Through the native Rebrickable API, this operation is `GET /lego/parts/:part_num/colors/:color_id/sets/` (base URL `https://rebrickable.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sets-containing-part-color.md) for the provider-specific parameters and requirements.

