# OkoCRM: Create deal

Creates a new deal in OkoCRM.

```
POST https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "pipeline_id": 1,
  "stages_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "pipeline_id": 1,
    "stages_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `budget` | string | no | Deal budget. |
| `name` | string | yes | Deal name. |
| `pipeline_id` | number | yes | The pipeline to create the deal in. |
| `stages_id` | number | yes | The starting stage for the new deal. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_id": 1,
      "lead": {},
      "lead_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_id` | number |  |
| `lead` | object |  |
| `lead_id` | number |  |

## Native endpoint

Through the native OkoCRM API, this operation is `POST /leads/` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

