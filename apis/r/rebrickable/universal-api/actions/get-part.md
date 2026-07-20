# Rebrickable: Get Part

Retrieves a LEGO part from Rebrickable by part number.

```
GET https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-part
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrickable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-part?connectionId=$CONNECTION_ID&partNum=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "partNum": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-part?${params}`, {
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
| `partNum` | string | yes | Rebrickable part number to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "external_ids": {},
      "molds": [
        {}
      ],
      "name": "Ava Chen",
      "part_cat_id": 1,
      "part_img_url": "https://example.com",
      "part_num": "string",
      "part_url": "https://example.com",
      "prints": [
        {}
      ],
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
| `external_ids` | object |  |
| `molds` | array<object> |  |
| `name` | string |  |
| `part_cat_id` | number |  |
| `part_img_url` | string |  |
| `part_num` | string |  |
| `part_url` | string |  |
| `prints` | array<object> |  |
| `year_from` | number |  |
| `year_to` | number |  |

## Native endpoint

Through the native Rebrickable API, this operation is `GET /lego/parts/:part_num/` (base URL `https://rebrickable.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-part.md) for the provider-specific parameters and requirements.

