# Datalyse: Create Lead

Creates a new contact or company in Datalyse.

```
POST https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datalyse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | no | Set to "unassigned" to assign this lead to all agents, or provide a specific agent_id to assign it to an agent (optional) |
| `companyLeadId` | string | no | ID of the company this contact belongs to (optional) |
| `country` | string | no | Country ISO code |
| `email` | string | no | Email |
| `isCompany` | string | no | Set to "y" if it is a company (optional) |
| `lastname` | string | no | Last name |
| `leadTypeId` | string | no | Identifier of the contact or company type (optional) |
| `name` | string | yes | Name for the contact |
| `note` | string | no | Add a note to this contact or company (optional) |
| `phone` | string | no | Phone with international prefix |
| `status` | string | no | Status ID Default: `0`. |

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

Through the native Datalyse API, this operation is `POST /api/1.0/leads/create.json` (base URL `https://api.datalyse.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

