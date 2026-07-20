# Halo Service Solutions: Get Quotation

Retrieves a quotation from Halo Service Solutions.

```
GET https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-quotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-quotation?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-quotation?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent_id": 1,
      "assigned_agent": 1,
      "client_id": 1,
      "client_name": "Ava Chen",
      "date": "2026-05-07T12:00:00.000Z",
      "expiry_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "note": "string",
      "site_id": 1,
      "site_name": "Ava Chen",
      "status": 1,
      "title": "string",
      "total": 1,
      "user_id": 1,
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent_id` | number |  |
| `assigned_agent` | number |  |
| `client_id` | number |  |
| `client_name` | string |  |
| `date` | date |  |
| `expiry_date` | date |  |
| `id` | number | Quotation ID |
| `note` | string |  |
| `site_id` | number |  |
| `site_name` | string |  |
| `status` | number |  |
| `title` | string |  |
| `total` | number |  |
| `user_id` | number |  |
| `user_name` | string |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `GET /Quotation/:id` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quotation.md) for the provider-specific parameters and requirements.

