# Rebrickable: Get Minifig

Retrieves a LEGO minifig from Rebrickable by set number.

```
GET https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-minifig
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrickable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-minifig?connectionId=$CONNECTION_ID&setNum=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "setNum": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-minifig?${params}`, {
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
| `setNum` | string | yes | Rebrickable minifig set number, such as fig-000001. |

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

Through the native Rebrickable API, this operation is `GET /lego/minifigs/:set_num/` (base URL `https://rebrickable.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-minifig.md) for the provider-specific parameters and requirements.

