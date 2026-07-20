# Rebrickable: List Minifig Parts

Retrieves parts for a LEGO minifig in Rebrickable.

```
GET https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-minifig-parts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrickable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-minifig-parts?connectionId=$CONNECTION_ID&limit=25&offset=0&setNum=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "setNum": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-minifig-parts?${params}`, {
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
| `setNum` | string | yes | Rebrickable minifig set number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": {},
      "id": 1,
      "inv_part_id": 1,
      "is_spare": true,
      "part": {},
      "quantity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | object |  |
| `id` | number |  |
| `inv_part_id` | number |  |
| `is_spare` | boolean |  |
| `part` | object |  |
| `quantity` | number |  |

## Native endpoint

Through the native Rebrickable API, this operation is `GET /lego/minifigs/:set_num/parts/` (base URL `https://rebrickable.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-minifig-parts.md) for the provider-specific parameters and requirements.

