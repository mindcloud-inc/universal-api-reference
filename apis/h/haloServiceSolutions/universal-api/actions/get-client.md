# Halo Service Solutions: Get Client

Retrieves a client from Halo Service Solutions.

```
GET https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-client?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-client?${params}`, {
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
| `id` | number | yes | Client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datecreated": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_vip": true,
      "main_site_id": 1,
      "main_site_name": "Ava Chen",
      "name": "Ava Chen",
      "stopped": 1,
      "taxable": true,
      "toplevel_id": 1,
      "trading_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datecreated` | date |  |
| `id` | number |  |
| `is_vip` | boolean |  |
| `main_site_id` | number |  |
| `main_site_name` | string |  |
| `name` | string |  |
| `stopped` | number |  |
| `taxable` | boolean |  |
| `toplevel_id` | number |  |
| `trading_name` | string |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `GET /Client/:id` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

