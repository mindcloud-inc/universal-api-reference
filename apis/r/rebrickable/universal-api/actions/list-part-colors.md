# Rebrickable: List Part Colors

Retrieves available colors for a LEGO part in Rebrickable.

```
GET https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-part-colors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrickable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-part-colors?connectionId=$CONNECTION_ID&limit=25&offset=0&partNum=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "partNum": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-part-colors?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "color_id": 1,
      "color_name": "Ava Chen",
      "elements": [
        "string"
      ],
      "num_set_parts": 1,
      "num_sets": 1,
      "part_img_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color_id` | number |  |
| `color_name` | string |  |
| `elements` | array<string> |  |
| `num_set_parts` | number |  |
| `num_sets` | number |  |
| `part_img_url` | string |  |

## Native endpoint

Through the native Rebrickable API, this operation is `GET /lego/parts/:part_num/colors/` (base URL `https://rebrickable.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-part-colors.md) for the provider-specific parameters and requirements.

