# Rebrickable: Get Part Color

Retrieves a LEGO part color from Rebrickable.

```
GET https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-part-color
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrickable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-part-color?connectionId=$CONNECTION_ID&partNum=string&colorId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "partNum": "string",
  "colorId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-part-color?${params}`, {
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
| `colorId` | number | yes | Rebrickable color ID for the part/color combination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "elements": [
        "string"
      ],
      "num_set_parts": 1,
      "num_sets": 1,
      "part_img_url": "https://example.com",
      "year_from": 1,
      "year_to": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `elements` | array<string> |  |
| `num_set_parts` | number |  |
| `num_sets` | number |  |
| `part_img_url` | string |  |
| `year_from` | number |  |
| `year_to` | number |  |

## Native endpoint

Through the native Rebrickable API, this operation is `GET /lego/parts/:part_num/colors/:color_id/` (base URL `https://rebrickable.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-part-color.md) for the provider-specific parameters and requirements.

