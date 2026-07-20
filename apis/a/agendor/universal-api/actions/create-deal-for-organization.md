# Agendor: Create Deal For Organization

Creates a new deal for an organization in Agendor.

```
POST https://connect.mindcloud.co/v1/universal/agendor/latest/actions/create-deal-for-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agendor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agendor/latest/actions/create-deal-for-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deal": "string",
  "organization_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agendor/latest/actions/create-deal-for-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deal": "string",
    "organization_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deal` | string | yes | Deal payload as a JSON string matching Agendor's create deal for organization body. |
| `organization_id` | number | yes | ID of the organization that will own the deal. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agendor API returns.

## Native endpoint

Through the native Agendor API, this operation is `POST /organizations/:organization_id/deals` (base URL `https://api.agendor.com.br/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal-for-organization.md) for the provider-specific parameters and requirements.

