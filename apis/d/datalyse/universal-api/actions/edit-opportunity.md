# Datalyse: Edit Opportunity

Updates an existing opportunity in Datalyse.

```
PUT https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/edit-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datalyse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/edit-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "opportunityId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/edit-opportunity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "opportunityId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | no | Agent ID or "unassigned" (optional) |
| `amount` | string | no | Total amount (optional) |
| `currency` | string | no | Currency (optional) |
| `description` | string | no | Description of the opportunity (optional) |
| `opportunityId` | string | yes | ID of the opportunity to edit |
| `pipeline` | string | no | Pipeline ID (optional) |
| `status` | string | no | Status ID (optional) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | API response status |

## Native endpoint

Through the native Datalyse API, this operation is `POST /api/1.0/opportunities/edit.json` (base URL `https://api.datalyse.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-opportunity.md) for the provider-specific parameters and requirements.

