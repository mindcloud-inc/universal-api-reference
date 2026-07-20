# Rebrickable: Get Set

Retrieves a LEGO set from Rebrickable by set number.

```
GET https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrickable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-set?connectionId=$CONNECTION_ID&setNum=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "setNum": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-set?${params}`, {
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
| `setNum` | string | yes | Rebrickable set number, such as 75192-1. |

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
| `last_modified_dt` | date |  |
| `name` | string |  |
| `num_parts` | number |  |
| `set_img_url` | string |  |
| `set_num` | string |  |
| `set_url` | string |  |
| `theme_id` | number |  |
| `year` | number |  |

## Native endpoint

Through the native Rebrickable API, this operation is `GET /lego/sets/:set_num/` (base URL `https://rebrickable.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-set.md) for the provider-specific parameters and requirements.

