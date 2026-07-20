# Rebrickable: Get Theme

Retrieves a LEGO theme from Rebrickable by ID.

```
GET https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-theme
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrickable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-theme?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-theme?${params}`, {
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
| `id` | number | yes | Unique Rebrickable theme ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "parent_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `parent_id` | number |  |

## Native endpoint

Through the native Rebrickable API, this operation is `GET /lego/themes/:id/` (base URL `https://rebrickable.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-theme.md) for the provider-specific parameters and requirements.

