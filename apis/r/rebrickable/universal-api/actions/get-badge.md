# Rebrickable: Get Badge

Retrieves a badge from Rebrickable by ID.

```
GET https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-badge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrickable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-badge?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/get-badge?${params}`, {
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
| `id` | number | yes | Unique Rebrickable badge ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "descr": "string",
      "id": 1,
      "level": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `descr` | string |  |
| `id` | number |  |
| `level` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Rebrickable API, this operation is `GET /users/badges/:id/` (base URL `https://rebrickable.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-badge.md) for the provider-specific parameters and requirements.

