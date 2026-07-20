# Pinghome: Update Incident

Updates an existing incident in Pinghome.

```
PUT https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "incidentId": "ea719d39-5dae-46f4-b85e-ed881772af2e",
  "name": "MindCloud Test Incident Updated",
  "description": "Updated by MindCloud action test",
  "urgency": "high"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-incident', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "incidentId": "ea719d39-5dae-46f4-b85e-ed881772af2e",
    "name": "MindCloud Test Incident Updated",
    "description": "Updated by MindCloud action test",
    "urgency": "high"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `incidentId` | string | yes | Incident ID to update. Example: `ea719d39-5dae-46f4-b85e-ed881772af2e`. |
| `status` | string | no | Incident lifecycle status. |
| `name` | string | yes | Updated incident name. Example: `MindCloud Test Incident Updated`. |
| `description` | string | yes | Updated incident description. Example: `Updated by MindCloud action test`. |
| `urgency` | string | yes | Updated incident urgency. Example: `high`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `PUT /incident-cmd/v1/incident/:id` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-incident.md) for the provider-specific parameters and requirements.

