# Halo Service Solutions: Create Quotation

Creates a new quotation in Halo Service Solutions.

```
POST https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-quotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-quotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-quotation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `[].title` | string | no |  |
| `[].client_id` | number | no |  |
| `[].user_id` | number | no |  |
| `[].agent_id` | number | no |  |
| `[].site_id` | number | no |  |
| `[].ticket_id` | number | no |  |
| `[].date` | date | no |  |
| `[].expiry_date` | date | no |  |
| `[].note` | string | no |  |

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

Through the native Halo Service Solutions API, this operation is `POST /Quotation` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quotation.md) for the provider-specific parameters and requirements.

